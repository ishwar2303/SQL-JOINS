## Create database
```sql
CREATE DATABASE BASIC;
```

## Use database
```sql
USE BASIC;
```

## Create table courses
```sql
CREATE TABLE COURSES (
	COURSE_ID INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
	COURSE_NAME VARCHAR(30) NOT NULL
);
```

## Create table colleges
```sql
CREATE TABLE COLLEGES (
	COLLEGE_ID INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
	COLLEGE_NAME VARCHAR(50) NOT NULL
);
```

## Create table students
```sql
CREATE TABLE STUDENTS (
	ID INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
	NAME VARCHAR(50) NOT NULL,
	EMAIL VARCHAR(50) NOT NULL UNIQUE,
	GENDER CHAR(1) NOT NULL,
	COLLEGE_ID INT,
	COURSE_ID INT 
);
```

## Add Foreign Constraints
```sql
ALTER TABLE STUDENTS ADD FOREIGN KEY (COURSE_ID) REFERENCES COURSES(COURSE_ID);
ALTER TABLE STUDENTS ADD FOREIGN KEY (COLLEGE_ID) REFERENCES COLLEGES(COLLEGE_ID);
```


## Insert records in courses table
```sql
INSERT INTO `courses` VALUES
(NULL, 'BE/B.Tech'),
(NULL, 'B.Arch'),
(NULL, 'BCA'),
(NULL, 'B.Sc'),
(NULL, 'BPharma'),
(NULL, 'BDS');
```

## Insert records in colleges table
```sql
INSERT INTO `colleges` VALUES
(NULL, 'AMITY INSTITUTE OF EDUCATION'),
(NULL, 'SRM UNIVERSITY'),
(NULL, 'INDIAN INSTITUTE OF TECHNOLOGY'),
(NULL, 'MANIPAL UNIVERSITY'),
(NULL, 'BIRLA INSTITUTE OF TECHNOLOGY'),
(NULL, 'DELHI UNIVERSITY');
```


## Insert records in students table
```sql
INSERT INTO `students` VALUES
(NULL, 'SAMEER', 'SAMEER.K@GMAIL.COM', 'M', 2, 3),
(NULL, 'KARAN', 'KARAN@GMAIL.COM', 'M', 1, 5),
(NULL, 'AJAY', 'AJAY@GMAIL.COM', 'M', 1, 2),
(NULL, 'VIJAY', 'VIJAY@GMAIL.COM', 'M', 2, 2),
(NULL, 'VISHAL', 'VISHAL@GMAIL.COM', 'M', 1, 5),
(NULL, 'SHUBHAM', 'SHUBHAM@GMAIL.COM', 'M', 3, 4),
(NULL, 'TRISHA', 'TRISHA@GMAIL.COM', 'F', 5, 1),
(NULL, 'TAPAS', 'TAPAS@GMAIL.COM', 'M', 5, 5),
(NULL, 'SUNDAR', 'SUNDAR@GMAIL.COM', 'M', 4, 4),
(NULL, 'JATIN', 'JATIN@GMAIL.COM', 'M', 1, 1),
(NULL, 'MARUT', 'MARUT@GMAIL.COM', 'M', 1, 4),
(NULL, 'RHYTHM', 'RHYTHM@GMAIL.COM', 'M', 4, 1),
(NULL, 'ARJUN', 'ARJUN@GMAIL.COM', 'M', 1, 3),
(NULL, 'BHEEM', 'BHEEM@GMAIL.COM', 'M', 4, 6),
(NULL, 'CHETAN', 'CHETAN@GMAIL.COM', 'M', 3, 6),
(NULL, 'DINESH', 'DINESH.S@GMAIL.COM', 'M', 6, 1),
(NULL, 'FARAN', 'FARAN.M@GMAIL.COM', 'M', 6, 3),
(NULL, 'HIMESH', 'HIMESH@GMAIL.COM', 'M', 6, 2),
(NULL, 'ISHAN', 'ISHAN@GMAIL.COM', 'M', 3, 5),
(NULL, 'MOHAN', 'MOHAN@GMAIL.COM', 'M', 3, 2),
(NULL, 'SURAJ', 'SURAJ@GMAIL.COM', 'M', 1, 1),
(NULL, 'NEERAJ', 'NEERAJ@GMAIL.COM', 'M', 1, 5),
(NULL, 'SAURAV', 'SAURAV@GMAIL.COM', 'M', 3, 4),
(NULL, 'SUNNY', 'SUNNY@GMAIL.COM', 'M', 5, 1),
(NULL, 'ABHISHEK', 'ABHISHEK@GMAIL.COM', 'M', 2, 2),
(NULL, 'PUNEET', 'PUNEET@GMAIL.COM', 'M', 1, 5),
(NULL, 'AMAN', 'AMAN@GMAIL.COM', 'M', 3, 4),
(NULL, 'DIVYANSH', 'DIVYANSH@GMAIL.COM', 'M', 4, 1),
(NULL, 'ABHIJEET', 'ABHIJEET@GMAIL.COM', 'M', 1, 3),
(NULL, 'JITENDRA', 'JITENDRA@GMAIL.COM', 'M', 4, 6),
(NULL, 'PAYAL', 'PAYAL@GMAIL.COM', 'F', 3, 6),
(NULL, 'RAVI', 'RAVI@GMAIL.COM', 'M', 1, 5),
(NULL, 'RITESH', 'RITESH@GMAIL.COM', 'M', 1, 2),
(NULL, 'RAHUL', 'RAHUL@GMAIL.COM', 'M', 2, 2),
(NULL, 'VAIBHAV', 'VAIBHAV@GMAIL.COM', 'M', 2, 3),
(NULL, 'ROHIT', 'ROHIT@GMAIL.COM', 'M', 1, 5),
(NULL, 'TANU', 'TANU@GMAIL.COM', 'F', 4, 6),
(NULL, 'SHEETAL', 'SHEETAL@GMAIL.COM', 'F', 3, 6),
(NULL, 'DINESH', 'DINESH@GMAIL.COM', 'M', 6, 1),
(NULL, 'FARAN', 'FARAN@GMAIL.COM', 'M', 6, 3),
(NULL, 'ANAJALI', 'ANJALI@GMAIL.COM', 'F', 6, 2),
(NULL, 'SONIA', 'SONIA@GMAIL.COM', 'F', 3, 5),
(NULL, 'MANAV', 'MANAV@GMAIL.COM', 'M', 6, 1),
(NULL, 'KOYAL', 'KOYAL@GMAIL.COM', 'F', 6, 3),
(NULL, 'PRAGYA', 'PRAGYA@GMAIL.COM', 'F', 6, 2),
(NULL, 'DINESH', 'DINESH.H@GMAIL.COM', 'M', 3, 5),
(NULL, 'RAJAN', 'RAJAN@GMAIL.COM', 'M', 3, 2),
(NULL, 'VEERU', 'VEERU@GMAIL.COM', 'M', 1, 1);
```

## View Students table
```sql
SELECT * FROM STUDENTS;
```
![STUDENTS TABLE](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/STUDENTS-TABLE.PNG)

## View Courses table
```sql
SELECT * FROM COURSES;
```
![STUDENTS TABLE](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/COURSES-TABLE.PNG)

## View Colleges table
```sql
SELECT * FROM COLLEGES;
```
![STUDENTS TABLE](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/COLLEGES-TABLE.PNG)

## JOIN Students and Colleges table to see which student belongs to which college
```sql
SELECT 
	*
FROM
STUDENTS AS S INNER JOIN COLLEGES AS C
ON
S.COLLEGE_ID = C.COLLEGE_ID;
```
![STUDENT-COLLEGE](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/STUDENT-COLLEGE-JOIN.PNG)

## JOIN Students and Courses table to see in which course a particular student has enrolled
```sql

SELECT 
	*
FROM
STUDENTS AS S INNER JOIN COURSES AS C
ON
S.COURSE_ID = C.COURSE_ID;
```
![STUDENT-COURSE](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/STUDENT-COURSE-JOIN.PNG)

## JOIN Students, Colleges and Courses to see which course is enrolled by student in the college
```sql

SELECT 
	*
FROM
STUDENTS AS S INNER JOIN COURSES AS COU
ON
S.COURSE_ID = COU.COURSE_ID
INNER JOIN COLLEGES AS COL
ON
S.COLLEGE_ID = COL.COLLEGE_ID;
```
![STUDENT-COLLEGE-COURSE](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/STUDENT-COLLEGE-COURSE.PNG)

## Use GROUP BY to group students by course
### To see Number of students enrolled in a particular course 
```sql
SELECT 
	COUNT(C.COURSE_ID) AS NUMBER_OF_STUDENTS,
	COURSE_NAME
FROM
STUDENTS S INNER JOIN COURSES C
ON
S.COURSE_ID = C.COURSE_ID
GROUP BY C.COURSE_ID;
```

## Use GROUP BY to group students by college
### To see Number of students in a particular college
```sql
SELECT 
	COUNT(C.COLLEGE_ID) AS NUMBER_OF_STUDENTS,
	COLLEGE_NAME
FROM
STUDENTS S INNER JOIN COLLEGES C
ON
S.COLLEGE_ID = C.COLLEGE_ID
GROUP BY C.COLLEGE_ID;
```
![NO-OF-STUDENTS-IN-COLLEGE](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/NUMBER-OF-STUDENTS-IN-A-COLLEGE.PNG)

## Total number of students
```sql
SELECT COUNT(ID) AS TOTAL_NUMBER_OF_STUDENTS_IN_ALL_COLLEGES FROM STUDENTS;
```
![NO-OF-STUDENTS](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/TOTAL-STUDENTS.PNG)

## Total number of male students
```sql
SELECT COUNT(ID) AS TOTAL_MALE_STUDENTS_IN_ALL_COLLEGES FROM STUDENTS WHERE GENDER = 'M';
```
![MALE](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/TOTAL-MALE-STUDENTS.PNG)

## Total number of female students 
```sql
SELECT COUNT(ID) AS TOTAL_FEMALE_STUDENTS_IN_ALL_COLLEGES FROM STUDENTS WHERE GENDER = 'F';
```
![FEMALE](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/TOTAL-FEMALE-STUDENTS.PNG)

## Number of male and female students college wise
```sql
SELECT
	COLLEGE_NAME,
	(SELECT COUNT(ID) FROM STUDENTS WHERE COLLEGE_ID = C.COLLEGE_ID AND GENDER = 'M') AS MALE_STUDENTS,
	(SELECT COUNT(ID) FROM STUDENTS WHERE COLLEGE_ID = C.COLLEGE_ID AND GENDER = 'F') AS FEMALE_STUDENTS
FROM
STUDENTS S INNER JOIN COLLEGES C
ON
S.COLLEGE_ID = C.COLLEGE_ID
GROUP BY C.COLLEGE_ID
ORDER BY C.COLLEGE_ID;
```
![MALE-FEMALE](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/NUMBER-OF-MALE-FEMALE-STUDENTS-COLLEGE-WISE.PNG)

## Number of students course wise in a college
```sql

SELECT 
	COLLEGE_NAME,
	COURSE_NAME,
	COUNT(COU.COURSE_ID) AS NUMBER_OF_STUDENTS
FROM
STUDENTS AS S INNER JOIN COURSES AS COU
ON
S.COURSE_ID = COU.COURSE_ID
INNER JOIN COLLEGES AS COL
ON
S.COLLEGE_ID = COL.COLLEGE_ID
GROUP BY COU.COURSE_ID, COL.COLLEGE_ID
ORDER BY COL.COLLEGE_ID;
```
![COURSE-WISE](https://github.com/ishwar2303/SQL-JOINS/blob/main/screenshots/NUMBER-OF-STUDENTS-COURSE-WISE-IN-A-COLLEGE.PNG)
