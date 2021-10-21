## TAXI_SERVICE
![Alt-текст](https://www.manchester-airport-guide.co.uk/content/uploads/sites/12/2019/11/taxi.png)

[Project purpose](#project-purpose)

[Project structure](#project-structure)

[Implementation details](#implementation-details)

[Launch guide](#launch-guide)

___
## 📝 Project purpose

### This web project represents a simple online service with basic features such as:
- Registration, login and logout
- Driver authentication
- Adding car, manufacturer and driver
- Set driver into car
- Display data about cars, manufacturers and drivers
---
## 🧐 Project structure

### The project uses N-tier architecture. Project structure is the following:

- **Models** 
- **DAO layer**, containing basic CRUD-operations for communication with the persistence layer
- **Service layer**, containing business-logic of the application
- **Servlets**, implementing client-server communication logic
- **JavaServer Pages**

---
## 🛠️ Implementation details

- **Dependency Injection** design pattern is used in the project - DAO and Service dependencies are injected during **runtime**
- User authentication are realized through **filters**
- Logging is implemented via **Log4j2 library**
- **Maven Checkstyle Plugin** are configured

---
## 💻 Launch guide

### To run this project you will need to use(install):

- [JDK 11 or higher](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
- [Apache Maven](https://maven.apache.org/download.cgi)
- [Apache Tomcat](https://tomcat.apache.org/download-90.cgi)
- [MySQL RDBMS](https://dev.mysql.com/downloads/installer)

Here are the **steps** for you to follow:

- [X] Add this project to your IDE as **Maven project**.
- [X] Add new **Tomcat Server** configuration and select war-exploded artifact to deploy. Set application _context parameter_ to "/".
- [X] If you decide to use the default **JDBC**-based **DAO** implementation:
    - Execute queries listed in _src/main/resources/init_db.sql_ in MySQL RDBMS in order to create the schema and all the tables required.
    - Enter your own data in _src/main/java/mate/util/ConnectionUtil.java_ class on lines **9-12**.
- [X] Run the project via **Tomcat** configuration.

First, you will need to register as a new driver.
After a successful login you will be able to inject a car, a manufacturer, set driver to car.
