<h1>Apply filters to SQL queries</h1>

<h2>Project Description</h2>
My organization is working to make their system more secure. It is my job to ensure the system is safe, investigate all potential security issues, and update employee computers as needed. The following steps provide examples of how I used SQL with filters to perform security-related tasks.<br />


<h2>Languages and Utilities Used</h2>

- <b>SQL</b> 
- <b>MariaDB</b>

<h2>Environments Used </h2>

- <b>Windows 11</b> (22H2)

<h2>Retrieve after hours failed login attempts:</h2>

<p align="left">
There was a potential security incident that occurred after business hours (after 18:00). All after hours login attempts that failed need to be investigated.
The following code demonstrates how I created a SQL query to filter for failed login attempts that occurred after business hours.
<br/><br/>
<img src="https://i.imgur.com/PG18fJx.png" height="100%" width="100%"/>
<br /><br/>
<p align="left">
 <b>The first part of the screenshot is my query, and the second part is a portion of the output. This query filters for failed login attempts that occurred after 18:00.<br/> </b>
<br/>•	First, I started by selecting all data from the log_in_attempts table. 
<br/>•	Then, I used a WHERE clause with an AND operator to filter my results to output only login attempts that occurred after 18:00 and were unsuccessful. 
<br/>•	The first condition is login_time > '18:00', which filters for the login attempts that occurred after 18:00. 
<br/>•	The second condition is success = FALSE, which filters for the failed login attempts. 

<h2>Retrieve login attempts on specific dates:</h2>

<p align="left">
<br/>A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated.
<br/>The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.
<br/><br/>
<img src="https://i.imgur.com/acVQ91Y.png" height="100%" width="100%"/>
<br />
<p align="left">
<b>The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08.</b><br/>
<br/>•	First, I started by selecting all data from the log_in_attempts table. 
<br/>•	Then, I used a WHERE clause with an OR operator to filter my results to output only login attempts that occurred on either 2022-05-09 or 2022-05-08. 
<br/>•	The first condition is login_date = '2022-05-09', which filters for logins on 2022-05-09.  
<br/>•	The second condition is login_date = '2022-05-08', which filters for logins on 2022-05-08.

<h2>Retrieve login attempts outside of Mexico:</h2>

<p align="left">
After investigating the organization’s data on login attempts, I believe there is an issue with the login attempts that occurred outside of Mexico. These login attempts should be investigated.
The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico. 
<br/><br/>
<img src="https://i.imgur.com/MLuuj1X.png" height="100%" width="100%"/>
<br /><br/>
<p align="left">
<b>The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred in countries other than Mexico. </b><br/>
<br/>•	First, I started by selecting all data from the log_in_attempts table. 
<br/>•	Then, I used a WHERE clause with NOT to filter for countries other than Mexico. I used LIKE with MEX% as the pattern to match because the dataset represents Mexico as MEX and MEXICO. 
<br/>•	The percentage sign (%) represents any number of unspecified characters when used with LIKE. 
  
<h2>Retrieve employees in Marketing:</h2>

<p align="left">
My team wants to update the computers for certain employees in the Marketing department. To do this, I have to get information on which employee machines to update.
The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Marketing department in the East building.
<br/><br/>
<img src="https://i.imgur.com/NCPQFrJ.png" height="100%" width="100%"/>
<br /><br/>
<p align="left">
<b>The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Marketing department in the East building.</b><br/>
<br/>•	First, I started by selecting all data from the employees table. 
<br/>•	Then, I used a WHERE clause with AND to filter for employees who work in the Marketing department and in the East building. 
<br/>•  I used LIKE with East% as the pattern to match because the data in the office column represents the East building with the specific office number. 
<br/>•	The first condition is the department = 'Marketing' portion, which filters for employees in the Marketing department. 
<br/>•	The second condition is the office LIKE 'East%' portion, which filters for employees in the East building.

<h2>Retrieve employees in Finance or Sales:</h2>

<p align="left">
The machines for employees in the Finance and Sales departments also need to be updated. Since a different security update is needed, I have to get information on employees only from these two departments.
The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Finance or Sales departments.
<br/><br/>
<img src="https://i.imgur.com/byseRn1.png" height="100%" width="100%"/>
<br /><br/>
<p align="left">
<b>The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Finance and Sales departments. </b><br/>
<br/>•	First, I started by selecting all data from the employees table. Then, I used a WHERE clause with OR to filter for employees who are in the Finance and Sales departments.
<br/>•	I used the OR operator instead of AND because I want all employees who are in either department. 
<br/>•	The first condition is department = 'Finance', which filters for employees from the Finance department. 
<br/>•	The second condition is department = 'Sales', which filters for employees from the Sales department.
  
<h2>Retrieve all employees not in IT:</h2>

<p align="left">
My team needs to make one more security update on employees who are not in the Information Technology department. To make the update, I first have to get information on these employees.
The following demonstrates how I created a SQL query to filter for employee machines from employees not in the  Information Technology department
<br/><br/>
<img src="https://i.imgur.com/yecfC9e.png" height="100%" width="100%"/>
<br /><br/>
<p align="left">
<b> The first part of the screenshot is my query, and the second part is a portion of the output. The query returns all employees not in the Information Technology department. </b><br/>
<br/>•	First, I started by selecting all data from the employees table. 
<br/>•	Then, I used a WHERE clause with NOT to filter for employees not in this department.
<br/>
  
<b>Summary</b>
I applied filters to SQL queries to get specific information on login attempts and employee machines. 
<br/>•	I used two different tables, log_in_attempts and employees. 
<br/>•	I used the AND, OR, and NOT operators to filter for the specific information needed for each task. 
<br/>•	I also used LIKE and the percentage sign (%) wildcard to filter for patterns.

  
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
