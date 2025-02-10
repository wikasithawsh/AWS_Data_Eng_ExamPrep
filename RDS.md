## AWS RDS Note | 2025-02-06

### Commonly used AWS Acronyms 

    ARN : Amazon Resource Name (unique identifier for AWS resources)\
    Aurora : Amazon Aurora (high-performance proprietary relational database service)\
    AZ : Availability Zone\
    CLI : Command-Line Interface (used to interact with AWS services)\
    DNS : Domain Name System (translates domain names to IP addresses, used for endpoint resolution in RDS)\
    DR : Disaster Recovery (process of restoring database services in case of failure)\
    EBS : Elastic Block Store (persistent storage for AWS EC2 and RDS)\
    HA : High Availability (systems design ensuring minimal downtime)\
    IAM : Identity and Access Management (AWS service for managing permissions)\
    JSON : JavaScript Object Notation (used for storing semi-structured data in relational databases)\
    Multi-AZ : A Database that is duplicated in multiple Azs\
    NoSQL : Not Only SQL (databases designed for unstructured or semi-structured data)\
    RDS : Relational Database Service (AWS-managed database service)\
    SQL : Structured Query Language (language for querying and managing relational databases)\
    VPC : Virtual Private Cloud (isolated network environment for AWS resources)\

### RDS : Relational Database Service
          Supports > MySql, MariaDB, PostgreSQL, Oracle, Aurora
          Since AWS RDS is a managed service, shell access to the db is not available
          RDS capacity depends on the DB engine 
          RDS can be monitored via cloud watch 

### RDS hints:  
          RDS is a managed service, it handles OS, but EC2 is not a managed service 
          To create RDS , default VPC is not a good option due to lack of security 
          
### RDS Networking & Subnet hints  
         
          
          
