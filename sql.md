1) Write an SQL query to print the first three characters of  FIRST_NAME from Worker table.
   Select substring(FIRST_NAME,1,3) from Worker;
2) Write an SQL query to find the position of the alphabet (‘a’) in the first name column ‘Amitabh’ from Worker table.
   Select INSTR(FIRST_NAME, BINARY'a') from Worker where FIRST_NAME = 'Amitabh';
3) Write an SQL query that fetches the unique values of DEPARTMENT from Worker table and prints its length.
   Select distinct length(DEPARTMENT) from Worker;
4) Write an SQL query to print the FIRST_NAME from Worker table after replacing ‘a’ with ‘A’.
   Select REPLACE(FIRST_NAME,'a','A') from Worker;
5) Write an SQL query to print the FIRST_NAME and LAST_NAME from Worker table into a single column COMPLETE_NAME. A space char should separate them.
   Select CONCAT(FIRST_NAME, ' ', LAST_NAME) AS 'COMPLETE_NAME' from Worker;
6) Write an SQL query to print details of the Workers whose FIRST_NAME contains ‘a’.
   Select * from Worker where FIRST_NAME like '%a%';
7) Write an SQL query to print details of the Workers who have joined in Feb’2014.
   Select * from Worker where year(JOINING_DATE) = 2014 and month(JOINING_DATE) = 2;
8) Write an SQL query to fetch worker names with salaries >= 50000 and <= 100000.
   SELECT CONCAT(FIRST_NAME, ' ', LAST_NAME) As Worker_Name, Salary FROM worker WHERE WORKER_ID IN (SELECT WORKER_ID FROM worker WHERE Salary BETWEEN 50000 AND 100000);
9) Write an SQL query to fetch the no. of workers for each department in the descending order.
   SELECT DEPARTMENT, count(WORKER_ID) No_Of_Workers FROM worker GROUP BY DEPARTMENT ORDER BY No_Of_Workers DESC;
