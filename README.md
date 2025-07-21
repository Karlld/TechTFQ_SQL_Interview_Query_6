**TechTFQ_SQL_Interview_Query_6**

You are given a table having the marks of one student in every test. 
You have to output the tests in which the student has improved his performance. 
For a student to improve his performance he has to score more than the previous test.
Provide 2 solutions, one including the first test score and second excluding it.

```sql
DROP TABLE IF EXISTS  student_tests;
CREATE TABLE student_tests (test_id INT, marks INT);

INSERT INTO student_tests VALUES(100, 55);
INSERT INTO student_tests VALUES(101, 55);
INSERT INTO student_tests VALUES(102, 60);
INSERT INTO student_tests VALUES(103, 58);
INSERT INTO student_tests VALUES(104, 40);
INSERT INTO student_tests VALUES(105, 50);

SELECT * FROM student_tests;
```

| test_id | marks |
|---------|-------|
| 100 |	55 |
| 101 |	55 |
| 102 |	60 |
| 103 |	58 |
| 104 |	40 |
| 105 |	50 |

