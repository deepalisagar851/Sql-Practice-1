# Sql-Practice-1

CREATE DATABASE Emp_Details;
USE Emp_Details;
CREATE TABLE Employees
(EmpID int,
Name varchar(25),
Salary int,
Address varchar(255),
City varchar(55));

INSERT INTO Employees (EmpID,Name, Salary, Address, City)
VALUES(101,'Rajini',18000, 'Sector-15', 'Noida'),
(102,'Ramesh',8000, 'Sector-62', 'Noida'),
(103,'Rohini', 19000,'Rasoolpur', 'Noida'),
(107,'Jayesh',20000, 'Rajiv Choak', 'New Delhi');
(001,'Ankit Kumar',12000 ,'Sector-62', 'Noida'),
(002,'Chandan Kumar',8000, 'Sector-62', 'Noida'),
(003,'Ashish Kumar',9000, 'Sector-63', 'Greater Noida'),
(0004,'Aashi Kumari',10000, 'Sector-62', 'Greater Noida'),
(0005,'Arushi',16000, 'Uttam Nagar', 'Delhi'),
(0006,'Muskan',18000, 'Sector-62', 'Noida'),
(0007,'Deepak', 19000,'Rasoolpur', 'Noida'),
(0008,'Upasana',20000, 'Rajiv Choak', 'New Delhi');

select*from Employees;

select*from Employees
where salary<10000;

select*from Employees
where salary>=9000 AND salary<15000;

SELECT * FROM Employees
WHERE Salary NOT BETWEEN 9000 AND 15000;

select*from Employees
WHERE Name LIKE 'r%';

select*from Employees
WHERE Name LIKE '%y';

select*from Employees
WHERE Name LIKE '%a%';

select*from Employees
where salary>(Select Salary from Employees
where name='Ram');

select*from Employees
WHERE Name LIKE '___';

select*from Employees
WHERE  Salary>=9000 AND  Name LIKE '%r%';

select*from Employees
WHERE EmpID LIKE '1%1';

alter table Employees add Deptno int;

UPDATE Employees SET Deptno=10 WHERE EmpID in(101,103,107);

UPDATE Employees SET Deptno=20 WHERE  Deptno IS NULL;

UPDATE Employees SET Salary=12000 WHERE Deptno=10 AND Name LIKE 'r%';

UPDATE Employees SET  Deptno=30 WHERE Name LIKE '_a%';

UPDATE Employees SET Salary=8500 WHERE Deptno Not in(10,20);

UPDATE Employees SET Salary=15000 WHERE Name LIKE '%m';

UPDATE Employees SET Salary=5500 WHERE Deptno LIKE '2%4';

UPDATE Employees SET Salary=25000 WHERE Salary<10000 AND Name LIKE '%a%' AND  Deptno=20;

UPDATE Employees SET Salary=10000 WHERE (Salary>=8500 OR Salary<=9000);
