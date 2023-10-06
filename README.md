# Ex-No-4-Creating-Procedures-using-PL-SQL


# AIM: To create a procedure using PL/SQL.


# Steps:


1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);

2. Create a procedure named as insert_employee data.

3. Inside the procdure block, write the query for inserting the values into the employee table.

4. End the procedure.


5. Call the insert_employee data procedure to insert the values into the employee table.


6. Display the employee table



# Program:

```
SQL> CREATE TABLE ep(
     empid NUMBER,
     empname VARCHAR(10),
     dept VARCHAR(10),
     salary NUMBER
    );
CREATE OR REPLACE PROCEDURE emp_data AS
    BEGIN
    INSERT INTO ep(empid,empname,dept,salary)
    values(1,'SHAKTHI','MD',10000000);
    INSERT INTO ep(empid,empname,dept,salary)
    values(2,'ARUN','HR',500000);
    INSERT INTO ep(empid,empname,dept,salary)
    values(3,'DHANUSH','IT',200000);
    COMMIT;
   FOR emp_rec IN (SELECT * FROM ep)LOOP
   DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
   ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
   END LOOP;
   END;
  /

```
# Output:

<img width="520" alt="image" src="https://github.com/AlluguriSrikrishnateja/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/118343892/dddf84a0-0855-4bad-9ee8-a72b0b916b59">






# Result:


THE PROGRAM HAS BEEN IMPLEMENTED SUCCESSFULLY



