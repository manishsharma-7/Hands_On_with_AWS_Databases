# Query Data with DynamoDB

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-databases-query)

**Author:** Manish Sharma  
**Email:** manishsharma7@hotmail.com

---

## Query Data with DynamoDB

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-query_733d9399)

---

## Introducing Today's Project!

### What is Amazon DynamoDB?

Amazon DynamoDB is a non-relational AWS database service that stores data in tables, where data is organized using items and attributes.

### How I used Amazon DynamoDB in this project

In today’s project, I used Amazon DynamoDB to create and load tables, ran queries using the AWS CLI and console, and processed transactions (i.e., executed multiple operations as one to manage related data).

### One thing I didn't expect in this project was...

One thing I didn’t expect in this project is that DynamoDB requires using the partition key when grouping results or finding data using attributes. When I tried to query using only attributes, I ran into errors.


### This project took me...

This project took me 1 hrs including documentation. 

---

## Querying DynamoDB Tables

A partition key is the primary identifier that DynamoDB uses to partition the items in its table. Every item must have a partition key, and its value must be unique unless the table also has a sort key.

A sort key is an optional secondary key that DynamoDB uses to search for items. If a table has a sort key, each item's primary key consists of both the partition key and the sort key. This means the partition key can be the same for multiple items as long as the sort key is unique.



![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-query_d105b0b0)

---

## Limits of Using DynamoDB

I ran into an error when I queried for all comments made by specific users because queries must use the table’s partition key. The “posted by” attribute I used to filter results was not the partition key.

Insights we can extract from our Comment table include all comments left on a single post, even sorted or filtered by common date and time. And, insights we can’t easily extract include all comments made by a specific user.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-query_cb3e260c)

---

## Running Queries with CLI

A query I ran in CloudShell was aws dynamodb get-item. This command retrieves an item from the table using the partition key value specified in the command.

Query options I can add to my query include consistent-read (which provides a strongly consistent read), projection-expression (to return only specific attributes), and return-consumed-capacity (which returns the number of capacity units consumed).

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-query_733d9399)

---

## Transactions

A transaction is a group of operations bundled together and executed as a single unit. For a transaction to succeed, all operations within it must process successfully.

I ran a transaction using AWS CLI commands in AWS CloudShell. This transaction performed two actions: first, it added a new item to a table, then it updated an item in the form table (increasing the comment count by one).

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-query_2f65f83e)

---

---
