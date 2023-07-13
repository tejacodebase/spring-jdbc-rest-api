## SETUP
1. Provide database connetion properties in the application.properties, application-dev.properties, and application-qa.properties files. <br>
   Depending on the **VM Options** you set, the database connection details will be set either DEV or QA.
2. Add VM Options
` -Dspring.profiles.active=dev `


## Contains
REST API using Spring Data JDBC
- REST Controllers exposing GET, POST, PUT, and DELETE methods with CRUD Operations of Employee, Department Entities.
- Service (Employee, Department) Classes for business logic.
- JDBC Reposities (Employee, Department) are for retrieving data from Database.
- Application Exception Handler using @ControllerAdvice for Exception Classes which are in package ` com.vm.springlab.exception `


## SQL Queries for creating tables in the database
**Employee**
```
CREATE TABLE `your_db_name`.`employee` (
  `uuid` VARCHAR(40) NOT NULL,
  `first_name` VARCHAR(100) NULL,
  `last_name` VARCHAR(100) NULL,
  `salary` DECIMAL(10) NULL,
  `date_of_birth` DATE NULL,
  `joined_date_time` DATETIME NULL,
  `manager_uuid` VARCHAR(45) NULL,
  `department_uuid` VARCHAR(45) NULL,
  PRIMARY KEY (`uuid`)); `
```
**Department**
```
CREATE TABLE `your_db_name`.`department` (
  `uuid` VARCHAR(40) NOT NULL,
  `name` VARCHAR(100) NULL,
  `head_uuid` VARCHAR(40) NULL,
  PRIMARY KEY (`uuid`));
  ```
