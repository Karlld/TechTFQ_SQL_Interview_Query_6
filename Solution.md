```sql
WITH prev_test AS (SELECT test_id,
                          marks,
                          LAG (marks, 1, 0) OVER (ORDER BY test_id) AS prev_marks
                      FROM student_tests
                   )

 SELECT test_id,
        marks
    FROM prev_test
    WHERE marks > prev_marks;

```



| test_id | marks |
|---------|-------|
| 100 |	55 |
| 102 |	60 |
| 105 |	50 |



```sql
WITH prev_test AS (SELECT test_id,
                          marks,
                          LAG (marks, 1, 0) OVER (ORDER BY test_id) AS prev_marks
                      FROM student_tests
                   )

  SELECT test_id,
         marks
     FROM prev_test
     WHERE marks > prev_marks
     AND prev_marks != 0;

```



| test_id | marks |
|---------|-------|
| 102 |	60 |
| 105 |	50 |
