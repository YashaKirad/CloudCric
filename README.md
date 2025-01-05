# CloudCric

**CloudCric** is a project that automates the calculation of Dream11 points for IPL players using an ETL pipeline built with AWS RDS, Python, and SQL. The system processes IPL data from every delivery since 2007, stores it in a scalable MySQL database on AWS RDS, and makes it available for machine learning model training and fast querying. This solution streamlines data management, enabling data scientists to utilize comprehensive, processed datasets for analytical insights and predictive modeling.

The project begins with setting up an AWS RDS MySQL database. Using the free tier template, a secure and scalable database is created with minimal configuration. To allow seamless data communication, inbound rules for the database are modified to permit all traffic for both IPv4 and IPv6 protocols. This ensures smooth connectivity for extraction, transformation, and loading operations.

Data extraction from AWS RDS is achieved by connecting to the database using Python’s `mysql.connector` library. After establishing a connection, queries are run to retrieve tables like `delivery`, `player`, and `player_captain`, which are converted into pandas DataFrames for further processing. This structured approach facilitates efficient manipulation and analysis of IPL data.

For uploading data to AWS RDS, the database is initialized using Python and configured with libraries like `pymysql` and `sqlalchemy`. Once connected, processed datasets are uploaded back into the database as new tables, such as `batter_points`. This step ensures that the refined data is readily accessible for fast querying and advanced analytics.

The project emphasizes scalability and user-friendliness. AWS RDS provides a robust backend for storing and querying large datasets, while Python’s flexibility allows dynamic data transformations. Additionally, the system ensures cost-effectiveness by leveraging AWS’s free-tier services and following best practices to prevent unintended expenses.

With CloudCric, IPL data is transformed into actionable insights for Dream11 points calculation and machine learning training. The platform demonstrates the seamless integration of cloud databases with Python for advanced data processing and analysis, offering a powerful solution for sports analytics.


