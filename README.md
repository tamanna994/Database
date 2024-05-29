## Employee Management
- Create employee table and used different types of query.
```dtd
CREATE TABLE EMPLOYEE
(
   EmpCode      INT(4),
   EmpFName     VARCHAR(255),
   EmpLName     VARCHAR(255),
   Job          VARCHAR(255),
   Manager      CHAR(4),
   HireDate     DATE,
   Salary       INT(6),
   Commission   INT(6),
   DEPTCODE     INT(2)
);

```

- Insert data into table
```dtd
INSERT INTO EMPLOYEE  
VALUES (9369, 'TONY', 'STARK', 'SOFTWARE ENGINEER', 7902, '1980-12-17', 2800,0,20),
       (9499, 'TIM', 'ADOLF', 'SALESMAN', 7698, '1981-02-20', 1600, 300,30),    
       (9566, 'KIM', 'JARVIS', 'MANAGER', 7839, '1981-04-02', 3570,0,20),
       (9654, 'SAM', 'MILES', 'SALESMAN', 7698, '1981-09-28', 1250, 1400, 30),
       (9782, 'KEVIN', 'HILL', 'MANAGER', 7839, '1981-06-09', 2940,0,10),
       (9788, 'CONNIE', 'SMITH', 'ANALYST', 7566, '1982-12-09', 3000,0,20),
       (9839, 'ALFRED', 'KINSLEY', 'PRESIDENT', 7566, '1981-11-17', 5000,0, 10),
       (9844, 'PAUL', 'TIMOTHY', 'SALESMAN', 7698, '1981-09-08', 1500,0,30),
       (9876, 'JOHN', 'ASGHAR', 'SOFTWARE ENGINEER', 7788, '1983-01-12',3100,0,20),
       (9900, 'ROSE', 'SUMMERS', 'TECHNICAL LEAD', 7698, '1981-12-03', 2950,0, 20),
       (9902, 'ANDREW', 'FAULKNER', 'ANAYLYST', 7566, '1981-12-03', 3000,0, 10),
       (9934, 'KAREN', 'MATTHEWS', 'SOFTWARE ENGINEER', 7782, '1982-01-23', 3300,0,20),
       (9591, 'WENDY', 'SHAWN', 'SALESMAN', 7698, '1981-02-22', 500,0,30),
       (9698, 'BELLA', 'SWAN', 'MANAGER', 7839, '1981-05-01', 3420, 0,30),
       (9777, 'MADII', 'HIMBURY', 'ANALYST', 7839, '1981-05-01', 2000, 200, NULL),
       (9860, 'ATHENA', 'WILSON', 'ANALYST', 7839, '1992-06-21', 7000, 100, 50),
       (9861, 'JENNIFER', 'HUETTE', 'ANALYST', 7839, '1996-07-01', 5000, 100, 50);

```


- Employee tables data view
- Query:
```dtd
SELECT * FROM employee;
```
```SQL
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
| EmpCode | EmpFName | EmpLName | Job               | Manager | HireDate   | Salary | Commission | DEPTCODE |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
|    9369 | TONY     | STARK    | SOFTWARE ENGINEER | 7902    | 1980-12-17 |   2800 |          0 |       20 |
|    9499 | TIM      | ADOLF    | SALESMAN          | 7698    | 1981-02-20 |   1600 |        300 |       30 |
|    9566 | KIM      | JARVIS   | MANAGER           | 7839    | 1981-04-02 |   3570 |          0 |       20 |
|    9654 | SAM      | MILES    | SALESMAN          | 7698    | 1981-09-28 |   1250 |       1400 |       30 |
|    9782 | KEVIN    | HILL     | MANAGER           | 7839    | 1981-06-09 |   2940 |          0 |       10 |
|    9788 | CONNIE   | SMITH    | ANALYST           | 7566    | 1982-12-09 |   3000 |          0 |       20 |
|    9839 | ALFRED   | KINSLEY  | PRESIDENT         | 7566    | 1981-11-17 |   5000 |          0 |       10 |
|    9844 | PAUL     | TIMOTHY  | SALESMAN          | 7698    | 1981-09-08 |   1500 |          0 |       30 |
|    9876 | JOHN     | ASGHAR   | SOFTWARE ENGINEER | 7788    | 1983-01-12 |   3100 |          0 |       20 |
|    9900 | ROSE     | SUMMERS  | TECHNICAL LEAD    | 7698    | 1981-12-03 |   2950 |          0 |       20 |
|    9902 | ANDREW   | FAULKNER | ANAYLYST          | 7566    | 1981-12-03 |   3000 |          0 |       10 |
|    9934 | KAREN    | MATTHEWS | SOFTWARE ENGINEER | 7782    | 1982-01-23 |   3300 |          0 |       20 |
|    9591 | WENDY    | SHAWN    | SALESMAN          | 7698    | 1981-02-22 |    500 |          0 |       30 |
|    9698 | BELLA    | SWAN     | MANAGER           | 7839    | 1981-05-01 |   3420 |          0 |       30 |
|    9777 | MADII    | HIMBURY  | ANALYST           | 7839    | 1981-05-01 |   2000 |        200 |     NULL |
|    9860 | ATHENA   | WILSON   | ANALYST           | 7839    | 1992-06-21 |   7000 |        100 |       50 |
|    9861 | JENNIFER | HUETTE   | ANALYST           | 7839    | 1996-07-01 |   5000 |        100 |       50 |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
```
- WHERE Clause:

  It is used to extract only those records that fulfill a specified condition.
```dtd
select * from employee where job = 'SALESMAN';
```
```SQL
+---------+----------+----------+----------+---------+------------+--------+------------+----------+
| EmpCode | EmpFName | EmpLName | Job      | Manager | HireDate   | Salary | Commission | DEPTCODE |
+---------+----------+----------+----------+---------+------------+--------+------------+----------+
|    9499 | TIM      | ADOLF    | SALESMAN | 7698    | 1981-02-20 |   1600 |        300 |       30 |
|    9654 | SAM      | MILES    | SALESMAN | 7698    | 1981-09-28 |   1250 |       1400 |       30 |
|    9844 | PAUL     | TIMOTHY  | SALESMAN | 7698    | 1981-09-08 |   1500 |          0 |       30 |
|    9591 | WENDY    | SHAWN    | SALESMAN | 7698    | 1981-02-22 |    500 |          0 |       30 |
+---------+----------+----------+----------+---------+------------+--------+------------+----------+
```
```dtd
select * from employee where MANAGER = 7839;
```
```SQL
+---------+----------+----------+---------+---------+------------+--------+------------+----------+
| EmpCode | EmpFName | EmpLName | Job     | Manager | HireDate   | Salary | Commission | DEPTCODE |
+---------+----------+----------+---------+---------+------------+--------+------------+----------+
|    9566 | KIM      | JARVIS   | MANAGER | 7839    | 1981-04-02 |   3570 |          0 |       20 |
|    9782 | KEVIN    | HILL     | MANAGER | 7839    | 1981-06-09 |   2940 |          0 |       10 |
|    9698 | BELLA    | SWAN     | MANAGER | 7839    | 1981-05-01 |   3420 |          0 |       30 |
|    9777 | MADII    | HIMBURY  | ANALYST | 7839    | 1981-05-01 |   2000 |        200 |     NULL |
|    9860 | ATHENA   | WILSON   | ANALYST | 7839    | 1992-06-21 |   7000 |        100 |       50 |
|    9861 | JENNIFER | HUETTE   | ANALYST | 7839    | 1996-07-01 |   5000 |        100 |       50 |
+---------+----------+----------+---------+---------+------------+--------+------------+----------+
```
```dtd
mysql> select * from employee where EmpCode = 9844;
```
```SQL
+---------+----------+----------+----------+---------+------------+--------+------------+----------+
| EmpCode | EmpFName | EmpLName | Job      | Manager | HireDate   | Salary | Commission | DEPTCODE |
+---------+----------+----------+----------+---------+------------+--------+------------+----------+
|    9844 | PAUL     | TIMOTHY  | SALESMAN | 7698    | 1981-09-08 |   1500 |          0 |       30 |
+---------+----------+----------+----------+---------+------------+--------+------------+----------+
```
- ORDER By Keyword:
  
  It is used to sort the result-set in ascending or descending order.
```dtd
select * from employee order by Salary DESC;
```
```SQL
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
| EmpCode | EmpFName | EmpLName | Job               | Manager | HireDate   | Salary | Commission | DEPTCODE |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
|    9860 | ATHENA   | WILSON   | ANALYST           | 7839    | 1992-06-21 |   7000 |        100 |       50 |
|    9839 | ALFRED   | KINSLEY  | PRESIDENT         | 7566    | 1981-11-17 |   5000 |          0 |       10 |
|    9861 | JENNIFER | HUETTE   | ANALYST           | 7839    | 1996-07-01 |   5000 |        100 |       50 |
|    9566 | KIM      | JARVIS   | MANAGER           | 7839    | 1981-04-02 |   3570 |          0 |       20 |
|    9698 | BELLA    | SWAN     | MANAGER           | 7839    | 1981-05-01 |   3420 |          0 |       30 |
|    9934 | KAREN    | MATTHEWS | SOFTWARE ENGINEER | 7782    | 1982-01-23 |   3300 |          0 |       20 |
|    9876 | JOHN     | ASGHAR   | SOFTWARE ENGINEER | 7788    | 1983-01-12 |   3100 |          0 |       20 |
|    9788 | CONNIE   | SMITH    | ANALYST           | 7566    | 1982-12-09 |   3000 |          0 |       20 |
|    9902 | ANDREW   | FAULKNER | ANAYLYST          | 7566    | 1981-12-03 |   3000 |          0 |       10 |
|    9900 | ROSE     | SUMMERS  | TECHNICAL LEAD    | 7698    | 1981-12-03 |   2950 |          0 |       20 |
|    9782 | KEVIN    | HILL     | MANAGER           | 7839    | 1981-06-09 |   2940 |          0 |       10 |
|    9369 | TONY     | STARK    | SOFTWARE ENGINEER | 7902    | 1980-12-17 |   2800 |          0 |       20 |
|    9777 | MADII    | HIMBURY  | ANALYST           | 7839    | 1981-05-01 |   2000 |        200 |     NULL |
|    9499 | TIM      | ADOLF    | SALESMAN          | 7698    | 1981-02-20 |   1600 |        300 |       30 |
|    9844 | PAUL     | TIMOTHY  | SALESMAN          | 7698    | 1981-09-08 |   1500 |          0 |       30 |
|    9654 | SAM      | MILES    | SALESMAN          | 7698    | 1981-09-28 |   1250 |       1400 |       30 |
|    9591 | WENDY    | SHAWN    | SALESMAN          | 7698    | 1981-02-22 |    500 |          0 |       30 |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
```
```dtd
select * from employee order by salary ASC;
```
```SQL
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
| EmpCode | EmpFName | EmpLName | Job               | Manager | HireDate   | Salary | Commission | DEPTCODE |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
|    9591 | WENDY    | SHAWN    | SALESMAN          | 7698    | 1981-02-22 |    500 |          0 |       30 |
|    9654 | SAM      | MILES    | SALESMAN          | 7698    | 1981-09-28 |   1250 |       1400 |       30 |
|    9844 | PAUL     | TIMOTHY  | SALESMAN          | 7698    | 1981-09-08 |   1500 |          0 |       30 |
|    9499 | TIM      | ADOLF    | SALESMAN          | 7698    | 1981-02-20 |   1600 |        300 |       30 |
|    9777 | MADII    | HIMBURY  | ANALYST           | 7839    | 1981-05-01 |   2000 |        200 |     NULL |
|    9369 | TONY     | STARK    | SOFTWARE ENGINEER | 7902    | 1980-12-17 |   2800 |          0 |       20 |
|    9782 | KEVIN    | HILL     | MANAGER           | 7839    | 1981-06-09 |   2940 |          0 |       10 |
|    9900 | ROSE     | SUMMERS  | TECHNICAL LEAD    | 7698    | 1981-12-03 |   2950 |          0 |       20 |
|    9788 | CONNIE   | SMITH    | ANALYST           | 7566    | 1982-12-09 |   3000 |          0 |       20 |
|    9902 | ANDREW   | FAULKNER | ANAYLYST          | 7566    | 1981-12-03 |   3000 |          0 |       10 |
|    9876 | JOHN     | ASGHAR   | SOFTWARE ENGINEER | 7788    | 1983-01-12 |   3100 |          0 |       20 |
|    9934 | KAREN    | MATTHEWS | SOFTWARE ENGINEER | 7782    | 1982-01-23 |   3300 |          0 |       20 |
|    9698 | BELLA    | SWAN     | MANAGER           | 7839    | 1981-05-01 |   3420 |          0 |       30 |
|    9566 | KIM      | JARVIS   | MANAGER           | 7839    | 1981-04-02 |   3570 |          0 |       20 |
|    9839 | ALFRED   | KINSLEY  | PRESIDENT         | 7566    | 1981-11-17 |   5000 |          0 |       10 |
|    9861 | JENNIFER | HUETTE   | ANALYST           | 7839    | 1996-07-01 |   5000 |        100 |       50 |
|    9860 | ATHENA   | WILSON   | ANALYST           | 7839    | 1992-06-21 |   7000 |        100 |       50 |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
```
- UPDATE Query :
  This statement is used to modify the existing records in a table
```dtd
UPDATE employee  SET EmpFName = 'Ishrat', EmpLName = 'Jahan' where EmpCode = 9369;
```
```SQL
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
| EmpCode | EmpFName | EmpLName | Job               | Manager | HireDate   | Salary | Commission | DEPTCODE |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
|    9369 | Ishrat   | Jahan    | SOFTWARE ENGINEER | 7902    | 1980-12-17 |   2800 |          0 |       20 |
|    9499 | TIM      | ADOLF    | SALESMAN          | 7698    | 1981-02-20 |   1600 |        300 |       30 |
|    9566 | KIM      | JARVIS   | MANAGER           | 7839    | 1981-04-02 |   3570 |          0 |       20 |
|    9654 | SAM      | MILES    | SALESMAN          | 7698    | 1981-09-28 |   1250 |       1400 |       30 |
|    9782 | KEVIN    | HILL     | MANAGER           | 7839    | 1981-06-09 |   2940 |          0 |       10 |
|    9788 | CONNIE   | SMITH    | ANALYST           | 7566    | 1982-12-09 |   3000 |          0 |       20 |
|    9839 | ALFRED   | KINSLEY  | PRESIDENT         | 7566    | 1981-11-17 |   5000 |          0 |       10 |
|    9844 | PAUL     | TIMOTHY  | SALESMAN          | 7698    | 1981-09-08 |   1500 |          0 |       30 |
|    9876 | JOHN     | ASGHAR   | SOFTWARE ENGINEER | 7788    | 1983-01-12 |   3100 |          0 |       20 |
|    9900 | ROSE     | SUMMERS  | TECHNICAL LEAD    | 7698    | 1981-12-03 |   2950 |          0 |       20 |
|    9902 | ANDREW   | FAULKNER | ANAYLYST          | 7566    | 1981-12-03 |   3000 |          0 |       10 |
|    9934 | Tamanna  | Noshi    | SOFTWARE ENGINEER | 7782    | 1982-01-23 |   3300 |          0 |       20 |
|    9591 | WENDY    | SHAWN    | SALESMAN          | 7698    | 1981-02-22 |    500 |          0 |       30 |
|    9698 | BELLA    | SWAN     | MANAGER           | 7839    | 1981-05-01 |   3420 |          0 |       30 |
|    9777 | MADII    | HIMBURY  | ANALYST           | 7839    | 1981-05-01 |   2000 |        200 |     NULL |
|    9860 | ATHENA   | WILSON   | ANALYST           | 7839    | 1992-06-21 |   7000 |        100 |       50 |
|    9861 | JENNIFER | HUETTE   | ANALYST           | 7839    | 1996-07-01 |   5000 |        100 |       50 |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
```
- Delete Query:
  This statement is used to delete existing records in a table
```dtd
 delete from employee where Manager = 7839;
```
```SQL
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
| EmpCode | EmpFName | EmpLName | Job               | Manager | HireDate   | Salary | Commission | DEPTCODE |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
|    9369 | Ishrat   | Jahan    | SOFTWARE ENGINEER | 7902    | 1980-12-17 |   2800 |          0 |       20 |
|    9499 | TIM      | ADOLF    | SALESMAN          | 7698    | 1981-02-20 |   1600 |        300 |       30 |
|    9654 | SAM      | MILES    | SALESMAN          | 7698    | 1981-09-28 |   1250 |       1400 |       30 |
|    9788 | CONNIE   | SMITH    | ANALYST           | 7566    | 1982-12-09 |   3000 |          0 |       20 |
|    9839 | ALFRED   | KINSLEY  | PRESIDENT         | 7566    | 1981-11-17 |   5000 |          0 |       10 |
|    9844 | PAUL     | TIMOTHY  | SALESMAN          | 7698    | 1981-09-08 |   1500 |          0 |       30 |
|    9876 | JOHN     | ASGHAR   | SOFTWARE ENGINEER | 7788    | 1983-01-12 |   3100 |          0 |       20 |
|    9900 | ROSE     | SUMMERS  | TECHNICAL LEAD    | 7698    | 1981-12-03 |   2950 |          0 |       20 |
|    9902 | ANDREW   | FAULKNER | ANAYLYST          | 7566    | 1981-12-03 |   3000 |          0 |       10 |
|    9934 | Tamanna  | Noshi    | SOFTWARE ENGINEER | 7782    | 1982-01-23 |   3300 |          0 |       20 |
|    9591 | WENDY    | SHAWN    | SALESMAN          | 7698    | 1981-02-22 |    500 |          0 |       30 |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
```
- Limit Query:
  This clause is used to specify the number of records to return.
```dtd
 select * from employee limit 5;
```
```SQL
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
| EmpCode | EmpFName | EmpLName | Job               | Manager | HireDate   | Salary | Commission | DEPTCODE |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
|    9369 | Ishrat   | Jahan    | SOFTWARE ENGINEER | 7902    | 1980-12-17 |   2800 |          0 |       20 |
|    9499 | TIM      | ADOLF    | SALESMAN          | 7698    | 1981-02-20 |   1600 |        300 |       30 |
|    9654 | SAM      | MILES    | SALESMAN          | 7698    | 1981-09-28 |   1250 |       1400 |       30 |
|    9788 | CONNIE   | SMITH    | ANALYST           | 7566    | 1982-12-09 |   3000 |          0 |       20 |
|    9839 | ALFRED   | KINSLEY  | PRESIDENT         | 7566    | 1981-11-17 |   5000 |          0 |       10 |
+---------+----------+----------+-------------------+---------+------------+--------+------------+----------+
```
- Between Query:
  This operator selects values within a given range
```dtd
 SELECT * FROM employee WHERE EmpCode BETWEEN 9499 AND 9535;
```
```SQL
+---------+----------+----------+----------+---------+------------+--------+------------+----------+
| EmpCode | EmpFName | EmpLName | Job      | Manager | HireDate   | Salary | Commission | DEPTCODE |
+---------+----------+----------+----------+---------+------------+--------+------------+----------+
|    9499 | TIM      | ADOLF    | SALESMAN | 7698    | 1981-02-20 |   1600 |        300 |       30 |
+---------+----------+----------+----------+---------+------------+--------+------------+----------+
```
- Join Query:
  This clause is used to combine rows from two or more tables, based on a related column between them 
##### Consider the two tables below as follows
```dtd
CREATE TABLE Students (
        Roll_No INT (25),
        Name CHAR (25),
        Address CHAR (25),
        Phone INT (25),
        Age Int (25)
    );
        INSERT INTO Students
         (Roll_No, Name, Address, Phone, Age)
         VALUES
         (1, 'Harsh', 'Dhaka',0192, 18),
         (2, 'Pratik', 'Khulna', 0164, 19),
         (3, 'Deep', 'Motijil', 0199, 17),
         (4, 'Akash', 'Banani', 0176, 18),
         (5, 'Rohit', 'Sylhet', 0175, 18),
         (6, 'Rahul', 'Borguna', 0198, 17),
         (7, 'Raj', 'Dhaka', 0173, 18);
```
```dtd
select * from students;
```
```SQL
+---------+--------+---------+-------+------+
| Roll_No | Name   | Address | Phone | Age  |
+---------+--------+---------+-------+------+
|       1 | Harsh  | Dhaka   |   192 |   18 |
|       2 | Pratik | Khulna  |   164 |   19 |
|       3 | Deep   | Motijil |   199 |   17 |
|       4 | Akash  | Banani  |   176 |   18 |
|       5 | Rohit  | Sylhet  |   175 |   18 |
|       6 | Rahul  | Borguna |   198 |   17 |
|       7 | Raj    | Dhaka   |   173 |   18 |
+---------+--------+---------+-------+------+
```
```dtd
CREATE TABLE StudentCourse (
     Course_ID INT (25),
     Roll_No INT(25)
        );
        INSERT INTO StudentCourse
        (Course_ID, Roll_No)
        VALUES
        (1, 1),
        (2, 2),
        (2, 3),
        (3, 4),
        (3, 5),
        (1, 8),
        (4, 9),
        (4, 10);
```
```dtd
select*from studentcourse;
```
```SQL
+-----------+---------+
| Course_ID | Roll_No |
+-----------+---------+
|         1 |       1 |
|         2 |       2 |
|         2 |       3 |
|         3 |       4 |
|         3 |       5 |
|         1 |       8 |
|         4 |       9 |
|         4 |      10 |
+-----------+---------+
```
```dtd
 select * from students join studentcourse on students.Roll_No = studentcourse.Roll_No;
```
```SQL
+---------+--------+---------+-------+------+-----------+---------+
| Roll_No | Name   | Address | Phone | Age  | Course_ID | Roll_No |
+---------+--------+---------+-------+------+-----------+---------+
|       1 | Harsh  | Dhaka   |   192 |   18 |         1 |       1 |
|       2 | Pratik | Khulna  |   164 |   19 |         2 |       2 |
|       3 | Deep   | Motijil |   199 |   17 |         2 |       3 |
|       4 | Akash  | Banani  |   176 |   18 |         3 |       4 |
|       5 | Rohit  | Sylhet  |   175 |   18 |         3 |       5 |
+---------+--------+---------+-------+------+-----------+---------+
```
```dtd
select * from students inner join studentcourse on students.Roll_No = studentcourse.Roll_No;
```
```SQL
+---------+--------+---------+-------+------+-----------+---------+
| Roll_No | Name   | Address | Phone | Age  | Course_ID | Roll_No |
+---------+--------+---------+-------+------+-----------+---------+
|       1 | Harsh  | Dhaka   |   192 |   18 |         1 |       1 |
|       2 | Pratik | Khulna  |   164 |   19 |         2 |       2 |
|       3 | Deep   | Motijil |   199 |   17 |         2 |       3 |
|       4 | Akash  | Banani  |   176 |   18 |         3 |       4 |
|       5 | Rohit  | Sylhet  |   175 |   18 |         3 |       5 |
+---------+--------+---------+-------+------+-----------+---------+
```
```dtd
select students.Name, students.Age, studentcourse.Course_ID from students inner join studentcourse on students.Roll_No = studentcourse.Roll_No;
```
```SQL
+--------+------+-----------+
| Name   | Age  | Course_ID |
+--------+------+-----------+
| Harsh  |   18 |         1 |
| Pratik |   19 |         2 |
| Deep   |   17 |         2 |
| Akash  |   18 |         3 |
| Rohit  |   18 |         3 |
+--------+------+-----------+
```
```dtd
select * from students left join studentcourse on students.Roll_No = studentcourse.Roll_No;
```
```SQL
+---------+--------+---------+-------+------+-----------+---------+
| Roll_No | Name   | Address | Phone | Age  | Course_ID | Roll_No |
+---------+--------+---------+-------+------+-----------+---------+
|       1 | Harsh  | Dhaka   |   192 |   18 |         1 |       1 |
|       2 | Pratik | Khulna  |   164 |   19 |         2 |       2 |
|       3 | Deep   | Motijil |   199 |   17 |         2 |       3 |
|       4 | Akash  | Banani  |   176 |   18 |         3 |       4 |
|       5 | Rohit  | Sylhet  |   175 |   18 |         3 |       5 |
|       6 | Rahul  | Borguna |   198 |   17 |      NULL |    NULL |
|       7 | Raj    | Dhaka   |   173 |   18 |      NULL |    NULL |
+---------+--------+---------+-------+------+-----------+---------+
```
```dtd
select students.Name, studentcourse.Course_ID from students left join studentcourse on students.Roll_No = studentcourse.Roll_No;
```
```SQL
+--------+-----------+
| Name   | Course_ID |
+--------+-----------+
| Harsh  |         1 |
| Pratik |         2 |
| Deep   |         2 |
| Akash  |         3 |
| Rohit  |         3 |
| Rahul  |      NULL |
| Raj    |      NULL |
+--------+-----------+
```
```dtd
select * from students right join studentcourse on students.Roll_No = studentcourse.Roll_no;
```
```SQL
+---------+--------+---------+-------+------+-----------+---------+
| Roll_No | Name   | Address | Phone | Age  | Course_ID | Roll_No |
+---------+--------+---------+-------+------+-----------+---------+
|       1 | Harsh  | Dhaka   |   192 |   18 |         1 |       1 |
|       2 | Pratik | Khulna  |   164 |   19 |         2 |       2 |
|       3 | Deep   | Motijil |   199 |   17 |         2 |       3 |
|       4 | Akash  | Banani  |   176 |   18 |         3 |       4 |
|       5 | Rohit  | Sylhet  |   175 |   18 |         3 |       5 |
|    NULL | NULL   | NULL    |  NULL | NULL |         1 |       8 |
|    NULL | NULL   | NULL    |  NULL | NULL |         4 |       9 |
|    NULL | NULL   | NULL    |  NULL | NULL |         4 |      10 |
+---------+--------+---------+-------+------+-----------+---------+
```
```dtd
select students.Name, studentcourse.Course_ID from students right join studentcourse on students.Roll_No = studentcourse.Roll_No;
```
```SQL
+--------+-----------+
| Name   | Course_ID |
+--------+-----------+
| Harsh  |         1 |
| Pratik |         2 |
| Deep   |         2 |
| Akash  |         3 |
| Rohit  |         3 |
| NULL   |         1 |
| NULL   |         4 |
| NULL   |         4 |
+--------+-----------+
```