# opendb
## This is a database that is aimed to handle transactional workloads (OLTP == Online Transaction Process)
The system will be designed such that it handles concurrent users using mechanisms such as locking, connection pooling and transaction management
### Schema and Data modelling
The system will accept one to one, one to many and many to many types of relationship.
Normalization will be used to reduce redundacy and denomalization will be utilized to optimize perfomance for heavy workloads.
Indexes are used to speed up queries but they will be used in moderation to avoid slowing down the system
The business logic will be embedded to the db via functions

### Perfomance and Storage Considerations
Caching mechanisms will be applied in order to ensure faster data transfer within the db
Indexes will also be fine tuned to enhance perfomance further
For large tables table partitioning will be used to make queries faster

### Transaction Handling
The database should ensure that all the ACID principles are followed with a logical replication for high availability

### Backup, Recovery and Fault Tolerance
Regular backups will be schedules in to the system. On top of that write ahead logs will be utilized so as to ensure a point in time recovery is possible.

### Security and Access Control
To keep user data secure principle of least privilege will be used with separate read only and read write roles.
SSL/ TLS will be used to encrypt data at rest.
Logging will be enabled for user access and sensitive operations for compliance and monitoring

### monitoring and maintainability
Perfomance logging will be used so as to detect issues early with regular updates so as to correct them.

## Starting the system
### To start the system
To create an executable for the system use this commands
```
    cmake ..
```
followed by
```
    cmake --build .
```
after that use
```
    ./opendb
```
This will start the system
