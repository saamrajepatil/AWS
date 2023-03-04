
Create mysql RDS using below doc as ref:


https://aws.amazon.com/premiumsupport/knowledge-center/rds-connect-ec2-bastion-host/

Install maria DB on EC2 to use mysql commands:

yum install mariadb

To connect RDS db created use RDS endpoint to connect as host and creds created during database creation.

mysql -h mydb.ccpuve7797jk.us-east-1.rds.amazonaws.com -P 3306 -u admin -p

AWSmaster2023

CREATE DATABASE Employee;

USE Employee;

CREATE TABLE Employee_Info (EmployeeID int,EmployeeName varchar(255),EmergencyContactName varchar(255),PhoneNumber int,Address varchar(255),City varchar(255),Country varchar(255));

INSERT INTO Employee_Info(EmployeeID, EmployeeName, EmergencyContactName, PhoneNumber, Address, City, Country)
VALUES ('06', 'Sanjana','Jagannath', '9921321141', 'Camel Street House No 12', 'Chennai', 'India');
 
INSERT INTO Employee_Info VALUES ('07', 'Sayantini','Praveen', '9934567654', 'Nice Road 21', 'Pune', 'India');

SELECT city FROM Employee_Info;
SELECT * FROM Employee_Info;

DROP DATABASE Employee;

