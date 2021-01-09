[`◀`](/) / [`Database Management Systems`](/s/dbms/) / [`MCQs`](/s/dbms/mcqs/) / `QP`

<hr />

**1. Lack of structural independence is the drawback of**

* [x] Network & Heirarchical Model
* [ ] Data Definition Model
* [ ] Object based Model
* [ ] Relational Model

**2. By default, the order by clause lists items in which order?**

```sql
SELECT name
FROM instructor
WHERE dept_name = 'Physics'
ORDER BY name;
```

* [ ] Descending
* [ ] Any
* [ ] Same
* [x] Ascending

**3. Trigger is special type of __________ procedure.** 

* [x] Stored 
* [ ] Function 
* [ ] View 
* [ ] Table

**4. Find the minimum number of tables required for the following ER diagram in relational model**

![](https://i.imgur.com/kVzVLKt.png)

* [x] 2 
* [ ] 3 
* [ ] 4 
* [ ] 5

**5. Consider the set of relations given below and the SQL query that follows**
```
Students: (Roll Number, Name, Date of Birth)
Courses: (Course Number, Course Name, Instructor)
Grades: (Roll Number, Course Number, Grade)
```
```sql
SELECT DISTINCT Name
FROM Students, Courses, Grades
WHERE Students.Roll_Number = Grades.Roll_Number
  AND Courses.Instructor = Sriram
  AND Courses.Course_Number = Grades.Course_Number
  AND Grades.Grade = A;
```

* [ ] Names of Students who have got an A grade in all courses taught by Sriram 
* [ ] Names of Students who have got an A grade in all courses 
* [x] Names of Students who have got an A grade in at least one of the courses taught by Sriram 
* [ ] Names of Students who have got an B grade in all courses taught by Sriram

**6. Consider the following relations**

```
student(id, name, address, gpa, sizeHS)
campus(location, enrollment, rank)
apply(id, location, date, major, decision)
```
    
Indentify the correct query to find name and address of all students with GPA > 3.7 and sizeHS < 1000

* [x] `Π(name), address(σ(GPA) > 3.7 ∧ sizeHS < 1000(student))`
* [ ] `σ(name), address (Π(GPA) > 3.7 ∧ sizeHS < 1000 (student))`
* [ ] `Π(name), address(σ(GPA) > 3.7 ∨ sizeHS < 1000 (student))`
* [ ] `σ(name), address (Π(GPA) > 3.7 ∨ sizeHS < 1000 (student))`

**7. \_\_\_\_\_ hides internal details of physical storage and targets on describing entities, data types, relationships, and constraints.**

* [ ] Internal Level
* [ ] External Level
* [x] Conceptual Schema
* [ ] Mapping Level

**8. The following SQL is which type of join** 

```sql
SELECT emp.eid, emp.ename, dept.dname
FROM emp, dept;
```

* [ ] Equi Join
* [ ] Outer Join
* [ ] Natural Join
* [x] Cartesian Product

**9. For any pincode, there is only one city and state. Also, for given street, city and state, there is just one pincode. In normalization terms, empdt1 is a relation in**

* [ ] 1NF only
* [x] 2NF, and hence also in 1NF
* [ ] 3NF, and hence also in 2NF and 1NF
* [ ] BCNF, and hence also in 3NF, 2NF, 1NF

**10. During the process of conversion of an ER diagram to relational model, primary key of a many to many binary relationship becomes**

* [ ] Foreign key of any one participating entity
* [ ] Primary key of any one participating entity
* [x] The union of the primary keys of participating entities
* [ ] The union of the primary key and foreign key of any one participating entity

**11. If attributes A and B determine attribute C, then it is also true that:**

* [ ] A → C
* [ ] B → C
* [x] (A, B) is a composite determinant
* [ ] C is a determinant

**12. If we consider the following transaction consisting two bank accounts as A and B Read(A);A=A-30;write(A);read(B);B=B+30;write(B). The condition that sum of the accounts A and B should remain constant is**

* [ ] Durability
* [x] Consistency
* [ ] Isolation
* [ ] Atomicity

**13. In timestamp ordering protocol every data item A is associated with timestamp values as**

* [ ] W-timestamp(A)
* [ ] R-timestamp(A)
* [x] R-timestamp(A) AND W-timestamp(A)
* [ ] R-timestamp(A) OR W-timestamp(A)

**14. Bank customer can withdraw money from bank account using ATM machine interfaces. Which type of user is a bank customer?**

* [x] Naïve user
* [ ] Application Developer
* [ ] DBA
* [ ] Programmer

**15. Consider two E-R models. Model A consists of a relationship named ‘teaches’ between two entities ‘Professor’ and ‘Subject’. Model B has an additional entity is called ‘Class’. ‘Professor’ and ‘Class’ are joined by a relationship called ‘takes’ while ‘Class’ and ‘Course’ entities are joined by a relationship called ‘of’. Which of the following is correct?**

* [ ] Model A leads to more tables than Model B does when translated to the relational model.
* [x] Model B leads to more tables than Model A does when translated to the relational model.
* [ ] Both models lead to same number of tables when translated to the relational model.
* [ ] Both models have same number of relationships.

**16. \_\_\_\_\_ clause is an additional filter that is applied to the result.**

* [ ] SELECT
* [ ] GROUP BY
* [x] HAVING
* [ ] ORDER BY

**17. Given the relations
`employee(name, salary, deptno), and department(deptno, deptname, address)`. Which of the following queries cannot be expressed using the basic relational algebra operations (σ, π, ×, ⋈, ∪, ∩, −)?**

* [ ] Department address of every employee
* [ ] Employees whose name is the same as their department name
* [x] The sum of all employee’s salaries
* [ ] All employees of a given department

**18. Two operations are said to be conflicting if:**

* [ ] They belong to different transactions and performs read on different data item
* [ ] They belong to different transactions and performs read on the same data item
* [ ] They belong to same transactions and performs write operation on the same data item
* [x] They belong to different transactions , They operate on the same data item and at least one of them is a write operation

**19. An update log record represented with these fields**

* [x] Transaction Identifier, Data Item, Old Value, New Value
* [ ] Transaction Identifier, Old Value, Data Item, New Value
* [ ] Transaction Identifier, Data Item, New Value, Old Value
* [ ] Transaction Identifier, Data Item, New Value

**20. Consider an entity Customer(Cust_id, UID, Acct_no, Name, Branch_id) with following attribute details**

```
1. Cust_id: Unique registration number of each registered customer
2. Aadhar_no: unique number at the national level for each citizen
3. Account_no: Unique account number at the bank. A customer can have multiple
accounts or joint accounts. This attributes stores the primary account number
4. Name: Name of the Student
5. Branch_id : Branch number of the bank
```

**Which of the following options is INCORRECT?**

* [x] Account_no is a candidate key
* [ ] Cust_id can be a primary key
* [ ] Aadhar_no is a candidate key if all students are from the same country
* [ ] If S is a superkey such that S ∩ Aadhar_no is NULL then S U Aadhar_no is also a superkey
