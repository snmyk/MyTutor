# MyTutor
The goal of this project is to create a web-based tool, and possibly also a mobile application, for managing the tutor and TA selection, allocation, and monitoring. 
# How to run MyTutorApp(Server):

## External Structures or services:
Dependencies for these are added in "pom.xml" file and are downloaded when the system is run or compiled 
- The Uses a MySQL database which can be locally or remote
- Makes connection to database using JDBC driver
- Has HttpSession management using JDBC and database
- Uses Spring framework Security with SecurityFilterChain, BcryptPasswordEncoder, JDBCHttpSession, etc
- Makes use of Google Email to send messages from the App
- Uses an IpInfo API for getting client geolocation
- Uses Local Storage and directory for creating, storing, and managing documents and files for Templates or web page use. These must be within src/resources folder.
- Java Runtime Environment (JRE)
- Uses Maven and Java 8 or higher (must be added or upgraded on the system to run the application on)

## Preparations:
1. Must have MyTutorDB sql dump with Database tables, fields, constraints and foreign keys configured
2. Create a database schema named "mytutordb" and run the mytutordb sql dump to add tables and fields
3. There must be atleast one record in the Database tables UserProfiles, LoginDetails and Administrators.
4. The LoginDetails role must be "ROLE_ADMIN".
5. A valid email address for the user in UserProfiles for resetting password.
Example: 
- INSERT INTO userprofiles (username, emailAddress) VALUES ("mytutoradmin","my2023tutor@gmail.com");
- INSERT INTO administrators (username) VALUES ("mytutoradmin");
- INSERT INTO logindetails (username, login password, role) VALUES ("mytutoradmin", "password","ROLE_ADMIN");
6. Have access to "mytutor2023@gmail.com" email

## Application properties:
### MySQL Database connection
1. You must provide the remote or local host address to your MySQL database to the created database schema.
2. Provide a datasource username and password for connection to your database schema
3. The connection should support multiple access and have administrative rights to it
4. Provide these details again on DBConnection.java file for the database connection using JDBC

### System Email
1. Provide mail host, port number, username(email address) and "App password" for the System email
2. Set the messageFrom parameter in EmailSenderService to the username you provided for your email address

### Location services
1. Add your ip key for the location service API
2. It makes use of services by IpInfo
3. Can sign up at [Ip Info site to register and get api key](https://ipinfo.io/)

## Compiling or Running the application:
1. Run the command "java -jar my-spring-boot-app-1.0.0.jar" on a command line if the jar file was provided
2. mvn clean install -U and mvn clean package (to build from java files and whole package with system files and get a jar)
3. 

## Access to the website
1.hostIpAddress:8080/login e.g. [Local Access login](http://localhost:8080/login), [remote access login](http://196.47.239.204:8080/login)

## Executing the code on VisualStudio

# Required packages:
1. Java Extension
2. Maven for Java
3. Spring boot dashboard
3. Spring boot Extension package
4. Spring boot initializer java support

# To Execute the program:
1. Add new Java Spring boot Project
3. Select 3.2.0 snapshot version
4. Name the package com.mytutor.demo
5. Clone the git project to the new spring boot project.
6. Follow the instructions under subtopic: Preparations- to build the database and Application properties subtopics-to connect to the database and send emails.



![Screenshot (213)](https://github.com/snmyk/MyTutor/assets/67907125/3c6c40e4-4b8a-4ab8-8561-644d34411063)


![Screenshot (254)](https://github.com/snmyk/MyTutor/assets/67907125/c6c4f32b-392d-40bd-b8ae-710870904132)


![Screenshot (257)](https://github.com/snmyk/MyTutor/assets/67907125/0bcf3808-bb32-4b43-8dbc-22ef22ce1c3e)



![Screenshot (258)](https://github.com/snmyk/MyTutor/assets/67907125/42cd4b56-3c4a-4f38-bc8a-dc56468065cb)





