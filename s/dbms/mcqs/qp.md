[`◀`](/) / [`Database Management Systems`](/s/dbms/) / `MCQs`

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
