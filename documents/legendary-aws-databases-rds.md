
# Visualize a Relational Database

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-databases-rds)

**Author:** Manish Sharma  
**Email:** manishsharma7@hotmail.com

---

## Visualise a Relational Database

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-rds_1fddb0b5)

---

## Introducing Today's Project!

### What is Amazon RDS?

Amazon RDS (Relational Database Service) is a managed service that allows you to create, operate, and scale relational databases in the cloud. It automates administrative tasks like backups and patching, making database management easier and letting you focus on building applications.

### How I used Amazon RDS in this project

In today’s project, I used Amazon RDS to create a database and populated it by connecting through MySQL Workbench. I also managed the security group to secure my RDS instance’s connection and linked it with QuickSight to visualize the data.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was the number of errors I would run into.

### This project took me...

I took me abou 2 hours to complete this project with documentation.

---

## In the first part of my project...

### Creating a Relational Database

In this step, I created my relational database using Amazon Aurora and RDS service, and I quickly configured it using the EasyCreate option.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-rds_43343546)

---

## Understanding Relational Databases

A relational database is a type of database that uses rows and colums to organize data.

### MySQL vs SQL

SQL is a standardized language used to manage, query, and manipulate data in relational database management systems (RDBMS) 
MySQL is an open-source RDBMS—software that stores and organizes data—and it uses SQL to perform operations on that data.

---

## Populating my RDS instance

In this step, I made my RDS instance publicly accessible so that MySQL Workbench running on my local machine could connect to my RDS in the cloud.

In this step, I updated the default security group associated with my RDS instance to allow inbound traffic on port 3306 from my local machine's IP address. This configuration enables MySQL Workbench, running on my local machine, to securely connect to the RDS instance in the cloud.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-rds_91b9fd1g)

---

## Using MySQL Workbench

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-rds_1fddb0b5)

In this step, I populated my database by creating tables using the CREATE TABLE command, inserting data with the INSERT INTO statement, and viewing the data using SELECT *.

---

## Connecting QuickSight and RDS

To connect my RDS instance to Amazon QuickSight, I modified the inbound rules of the associated security group to allow traffic from QuickSight's IP ranges and selected the RDS instance when creating a new dataset.

This solution is risky because any external user, tool, or service can access my RDS instance.

### A better strategy

First, I made a new security group so that QuickSight can access my RDS intance.

Next, I connected my new security group to QuickSight by adding an inline policy explicitly allowing QuickSight to access the security group.

---

## Now to secure my RDS instance

To secure my RDS instance, I made it private and added an inbound rule to allow connections from the security group I created for a secure RDS and QuickSight connection.

I ensured that my RDS instance could be accessed by QuickSight by adding the appropriate RDS security groups to it.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-rds_1709b26b)

---

## Adding RDS as a data source for QuickSight

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-rds_1709b29b)

This data source differs from my initial one because it is not publicly accessible, but accessed through the security group.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-rds_1709b30b)

---

---
