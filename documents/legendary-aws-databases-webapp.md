# Connect a Web App with Aurora

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-databases-webapp)

**Author:** Manish Sharma  
**Email:** manishsharma7@hotmail.com

---

## Connect a Web App to Amazon Aurora

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-webapp_1709b26b)

---

## Introducing Today's Project!

### What is Amazon Aurora?

Amazon Aurora is a type of relational database that is useful for large-scale applications because it uses clusters to improve performance and scalability.

### How I used Amazon Aurora in this project

In today's project, I used Amazon Aurora to connect to the web app where I could add the data in the web app and it would store in the database.

### One thing I didn't expect in this project was...

One thing I didn’t expect in this project was how tangible databases are—being able to actually see the data I entered.

### This project took me...

It took me about 90 mins including time to write the documention. 

---

## Creating a Web App

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-webapp_b7999168)

To connect to my EC2 instance, I used the terminal with the SSH command (ssh -i "NextWorkAuroraApp.pem" ec2-user@ec2-54-179-1-153.ap-southeast-1.compute.amazonaws.com) and made sure I had the necessary permissions by running the command (chmod 400).

To help me create my web app, I first updated all the software on my EC2 instance and installed the necessary tools (Apache, PHP, PHP libraries, and MariaDB) to start the web app.

---

## Connecting my Web App to Aurora

I set up my EC2 instance’s connection details to my database through the terminal by editing the dbinfo.inc file using Nano.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-webapp_1709b25b)

---

## My Web App Upgrade

Next, I upgraded my web app by adding a sample PHP page with a header. It looks like a form that allows me to input data.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-webapp_2709b25b)

---

## Testing my Web App

To ensure my web app was working correctly, I used the MySQL CLI to verify that I could retrieve all the data I had entered through the web app.

![Image](http://learn.nextwork.org/elated_cyan_peaceful_duck/uploads/aws-databases-webapp_1409z22b)

---

---
