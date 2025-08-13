# Load Data into DynamoDB

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-databases-dynamodb)

**Author:** Manish Sharma  
**Email:** manishsharma7@hotmail.com

---

## Load Data into a DynamoDB Table

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-dynamodb_b481c730)

---

## Introducing Today's Project!

### What is Amazon DynamoDB?

Amazon DynamoDB is a non-relational database service from AWS that organizes data using key-value pairs.

### How I used Amazon DynamoDB in this project

In today’s project, I used Amazon DynamoDB to create five tables, utilized CloudShell and the CLI to quickly load data into our tables, and compared DynamoDB to relational databases to better understand how attributes work.

### One thing I didn't expect in this project was...

One thing I didn’t expect in this project was that we can perform many actions using the AWS CLI instead of the console, such as creating tables and data, reading data, and deleting tables or data.

### This project took me...

This project took me 60 minutes, including documentation time.

---

## Create a DynamoDB table

DynamoDB tables organize data using items and attributes. Each item is recorded as a set of attributes. An item can have any number of attributes, but must have at least one— the partition key.

An attribute is a piece of data about an item in a DynamoDB table. For example, if the item is a specific student, attributes can include student name, project completion status, email, and sign-up date. The number of attributes is flexible.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-dynamodb_a3cefee0)

---

## Read and Write Capacity

Read Capacity Units (RCUs) and Write Capacity Units (WCUs) measure my DynamoDB table's performance. DynamoDB pricing is based on the amount of RCUs and WCUs consumed—the more consumed, the higher the cost of the project.

Amazon DynamoDB's Free Tier covers 25 RCUs and WCUs. I turned off auto scaling because it can increase charges if DynamoDB automatically scales up my operations, resulting in higher RCU and WCU usage.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-dynamodb_ef47dd8f)

---

## Using CLI and CloudShell

AWS CloudShell is an environment that lets us run code to interact with our AWS resources and services. It’s convenient because AWS CLI is already installed and ready to use.

AWS CLI is software that lets you interact with AWS resources using commands instead of clicking through the console. It’s a practical tool preferred over the AWS Management Console for day-to-day engineering operations in the real world.

I ran the AWS CLI command aws dynamodb create-table in AWS CloudShell to create four new DynamoDB tables. I was able to define table names and attributes all within the command.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-dynamodb_81e0258b)

---

## Loading Data with CLI

I ran an AWS CLI command in AWS CloudShell to load multiple items into the DynamoDB table I set up in the previous step. The command is structured as:
aws dynamodb batch-write-item --request-items file://ContentCatalog.json

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-dynamodb_791c600b)

---

## Observing Item Attributes

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-dynamodb_b481c731)

I checked a ContentCatalog item, which had the following attributes: ID, Authors, ContentType, Difficulty, Price, ProjectCategory, Published, Title, and URL.

I checked another ContentCatalog item, which had a different set of attributes, including service, title, video type, and more.

---

## Benefits of DynamoDB

A benefit of DynamoDB over relational databases is its flexibility, as each item can have its own set of attributes. This is great for scenarios where a table holds different kinds of data and some attributes don’t apply to others.

Another benefit over relational databases is speed, because DynamoDB quickly partitions data to narrow down searches using the partition key. This is faster than relational databases, which often need to scan the entire table to find specific data.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-dynamodb_b481c730)

---

---
