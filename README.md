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
  The first part of the screenshot is my query, and the second part is a portion of the output. This query filters for failed login attempts that occurred after 18:00. 
<br/>•	First, I started by selecting all data from the log_in_attempts table. 
<br/>•	Then, I used a WHERE clause with an AND operator to filter my results to output only login attempts that occurred after 18:00 and were unsuccessful. 
<br/>•	The first condition is login_time > '18:00', which filters for the login attempts that occurred after 18:00. 
<br/>•	The second condition is success = FALSE, which filters for the failed login attempts. 

<h2>Retrieve login attempts on specific dates:</h2>

<p align="left">
<br/>A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated.
<br/>The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.
<br/>
  
<img src="https://i.imgur.com/PG18fJx.png" height="100%" width="100%"/>
<br />
<p align="left">
  The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08.  
<br/>•	First, I started by selecting all data from the log_in_attempts table. 
<br/>•	Then, I used a WHERE clause with an OR operator to filter my results to output only login attempts that occurred on either 2022-05-09 or 2022-05-08. 
<br/>•	The first condition is login_date = '2022-05-09', which filters for logins on 2022-05-09.  
<br/>•	The second condition is login_date = '2022-05-08', which filters for logins on 2022-05-08.

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
