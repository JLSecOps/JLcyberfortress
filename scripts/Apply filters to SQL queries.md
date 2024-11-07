# Apply filters to SQL queries

## Project description

In this project, I used SQL filtering to investigate potential security issues related to login attempts and employee machines. My goal was to examine data from the employees and log\_in\_attempts tables to retrieve specific records based on various conditions, such as time of login, country of origin, and employee department.

## Retrieve after-hours failed login attempts

**Query:**

- SELECT \* FROM log\_in\_attempts  
  - WHERE login\_time \> '18:00:00' AND success \= 0;

-  I used this query to identify all failed login attempts that occurred after 18:00. The `WHERE` clause filters records where `login_time` is greater than '18:00:00' and `success` is `0`, indicating a failed attempt. This helped me pinpoint potentially suspicious activities outside of regular business hours.

## Retrieve login attempts on specific dates

**Query:**

- SELECT \* FROM log\_in\_attempts  
  - WHERE login\_date \= '2022-05-09' OR login\_date \= '2022-05-08';

- I created this query to review all login attempts that occurred on '2022-05-09' and '2022-05-08'. The OR operator was used to specify either of these dates in the login\_date column. This allowed me to focus on login activity around a suspicious event.

## Retrieve login attempts outside of Mexico

**Query:**

- SELECT \* FROM log\_in\_attempts  
  - WHERE country NOT LIKE 'MEX%';  
-  I utilized this query to find all login attempts that did not originate from Mexico. By using the NOT LIKE operator with the pattern 'MEX%', I was able to exclude entries where the country column starts with 'MEX', which covers both 'MEX' and 'MEXICO'.

## Retrieve employees in Marketing

**Query:**

- SELECT \* FROM employees  
  - WHERE department \= 'Marketing' AND office LIKE 'East-%';  
- This query was used to retrieve all employees in the Marketing department who are located in the East building. The AND operator ensured that both conditions were met: the department being 'Marketing' and the office starting with 'East-'.

## Retrieve employees in Finance or Sales

**Query:**

- SELECT \* FROM employees  
  - WHERE department \= 'Finance' OR department \= 'Sales';  
- I designed this query to find all employees in either the Finance or Sales departments. The OR operator allowed me to select records where the department column matches either 'Finance' or 'Sales'.

## Retrieve all employees not in IT

**Query:**

- SELECT \* FROM employees  
  - WHERE department NOT LIKE 'Information Technology';  
- This query was used to identify all employees who are not part of the Information Technology department. By using the NOT LIKE operator, I could exclude records where the department column is 'Information Technology'.

## Summary

Through this project, I utilized SQL queries to filter and retrieve specific records from the log\_in\_attempts and employees tables. These queries allowed me to investigate failed login attempts after business hours, review login activities on specific dates, and exclude login attempts from certain locations. More importantly, they played a crucial role in gathering information on employees based on their department or office location, which in turn, helped with targeted security updates. This process was not just important, but crucial in maintaining system security and ensuring appropriate access controls.  
