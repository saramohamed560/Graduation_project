# Face-Recognition-Login-System
It's a Face Recognition Login System which is developed using Python Tkinter and MySQL database.


To successfully launch the project in your system, first, you must create the following database, and tables and declare some default data there. I'm assuming the MySQL server is installed in your system and you know the basics.


1. Create a database with this name, "employee_management"

create database employee_management;


2. Now create a table ("employee_register") under that database.

create table employee_register(
f_name VARCHAR(40) NOT NULL,
l_name VARCHAR(40) NOT NULL,
uid Int NOT NULL AUTO_INCREMENT,
email VARCHAR NOT NULL,
designation VARCHAR NOT NULL,
contact BIGINT NOT NULL,
dob DATE NOT NULL,
join_date DATE NOT NULL,
gender char(15) NOT NULL,
address VARCHAR NOT NULL,
PRIMARY KEY ( uid )
);


3. Run this command
Since we have set the user id as Integer type and Auto Increment (see the previous section), here we will set a base value for it so that the counting starts from that range.

ALTER TABLE employee_register AUTO_INCREMENT=1000;


4. Create an another table ("admin") there

create table admin(
username VARCHAR NOT NULL,
password VARCHAR NOT NULL,
PRIMARY KEY ( username )
);


5. Insert default value into the "admin" table
In this case, we are setting a user id and password for the admin of the system. You need to choose this credential as per your choice here.

INSERT INTO admin (username,password) VALUES ('your_username','your_password');

