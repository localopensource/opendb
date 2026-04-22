# opendb
## This is a database that is aimed to handle transactional workloads (OLTP)
### Schema and Data modelling
The system will accept one to one, one to many and many to many types of relationship.
Normalization will be used to reduce redundacy and denomalization will be utilized to optimize perfomance for heavy workloads.
Indexes are used to speed up queries but they will be used in moderation to avoid slowing down the system
The business logic will be embedded to the db via functions

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
