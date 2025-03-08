Default sql commands:
```sql
1. SELECT: Выбирает данные из таблиц
   SELECT column1, column2, ... FROM table_name;

2. INSERT: Вставляет новые данные в таблицу
   INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...);

3. UPDATE: Изменяет существующие данные в таблице
   UPDATE table_name SET column1 = value1, column2 = value2, ... WHERE condition;

4. DELETE: Удаляет данные из таблицы
   DELETE FROM table_name WHERE condition;

5. CREATE TABLE: Создает новую таблицу
   CREATE TABLE table_name (column1 datatype, column2 datatype, ...);

6. ALTER TABLE: Изменяет структуру существующей таблицы
   ALTER TABLE table_name ADD column_name datatype;

7. DROP TABLE: Удаляет таблицу
   DROP TABLE table_name;

8. CREATE INDEX: Создает индекс
   CREATE INDEX index_name ON table_name (column1, column2, ...);

9. EXPLAIN: Показывает план выполнения запроса
   EXPLAIN SELECT ... FROM ...;

10. TRANSACTION: Группа последовательных операций
    BEGIN; [операции] COMMIT; или ROLLBACK;

11. WHERE: Фильтрует строки
    SELECT ... FROM ... WHERE condition;

12. GROUP BY: Группирует строки
    SELECT ... FROM ... GROUP BY column1, column2, ...;

13. HAVING: Фильтрует группы
    SELECT ... FROM ... GROUP BY ... HAVING condition;

14. ORDER BY: Сортирует результат
    SELECT ... FROM ... ORDER BY column1 [ASC|DESC], ...;

15. LIMIT: Ограничивает количество возвращаемых строк
    SELECT ... FROM ... LIMIT number;

16. INNER JOIN: Возвращает строки при совпадении в обеих таблицах
    SELECT ... FROM table1 INNER JOIN table2 ON table1.column = table2.column;

17. LEFT JOIN: Возвращает все строки из левой таблицы и совпадающие из правой
    SELECT ... FROM table1 LEFT JOIN table2 ON table1.column = table2.column;

18. RIGHT JOIN: Возвращает все строки из правой таблицы и совпадающие из левой
    SELECT ... FROM table1 RIGHT JOIN table2 ON table1.column = table2.column;

19. FULL OUTER JOIN: Возвращает строки при совпадении в одной из таблиц
    SELECT ... FROM table1 FULL OUTER JOIN table2 ON table1.column = table2.column;

20. CROSS JOIN: Возвращает декартово произведение двух таблиц
    SELECT ... FROM table1 CROSS JOIN table2;
```

```sql
Агрегирующие функции:
1. COUNT(): Подсчитывает количество строк
   SELECT COUNT(*) FROM table_name;

2. SUM(): Вычисляет сумму значений
   SELECT SUM(column_name) FROM table_name;

3. AVG(): Вычисляет среднее значение
   SELECT AVG(column_name) FROM table_name;

4. MAX(): Находит максимальное значение
   SELECT MAX(column_name) FROM table_name;

5. MIN(): Находит минимальное значение
   SELECT MIN(column_name) FROM table_name;


Математические операции:
1. CEILING(): Округляет до ближайшего большего целого
   SELECT CEILING(number);

2. FLOOR(): Округляет до ближайшего меньшего целого
   SELECT FLOOR(number);

3. ROUND(): Округляет до ближайшего целого или указанного количества десятичных знаков
   SELECT ROUND(number, decimals);

4. ABS(): Возвращает абсолютное значение
   SELECT ABS(number);

5. POWER(): Возводит число в степень
   SELECT POWER(base, exponent);

6. SQRT(): Вычисляет квадратный корень
   SELECT SQRT(number);

7. RANDOM(): Генерирует случайное число от 0 до 1
   SELECT RANDOM();

8. PI(): Возвращает значение π
   SELECT PI();

9. EXP(): Возвращает экспоненту
   SELECT EXP(number);

10. LN(): Вычисляет натуральный логарифм
    SELECT LN(number);
```

