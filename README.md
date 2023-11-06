# Ex. No: 4 Creating Procedures using PL/SQL
## DATE:
### AIM: 
 To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```sql

create table vacancy (
empid number,
empname varchar (15),
dept varchar(15),
salary number
);

create or replace procedure insert_vacancy_data as

begin

insert into vacancy (empid, empname, dept, salary) values (001,'Lucas Warren', 'Architect', 640000);

insert into vacancy (empid, empname, dept, salary) values (002,'Melaine Bailey', 'Interpreter', 180700);

insert into vacancy (empid, empname, dept, salary) values (003,'Tyler Dalton', 'Geologist', 560100);

insert into vacancy (empid, empname, dept, salary) values (004,'Ryan Gosling', 'Meteorologist', 165200);

commit;


for emp_rec IN (select * from vacancy) LOOP

dbms_output.put_line('Employee ID: ' || emp_rec.empid || ',Employee Name: ' || emp_rec.empname || ',Department: ' || emp_rec.dept || ',Salary:' || emp_rec.salary);

end loop;

end;
/


 begin
 insert_vacancy_data;
 end;
  /


SQL> select *from vacancy;
```


### Output:
![dbms ex-04 output](https://github.com/SudharsanamRK/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/115523484/fb150046-c9fd-42d8-9769-bb5982b5f0a7)


### Result:
Thus To create a procedure using PL/SQL has been done successfully.
