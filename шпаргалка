**Типы данных в PostgreSQL**

1. **Числовые типы:**
   - **Целые числа:** `SMALLINT`, `INTEGER`, `BIGINT`.
   - **Дробные числа:** `DECIMAL`, `NUMERIC`, `REAL`, `DOUBLE PRECISION`.
   - **Последовательности:** `SERIAL`, `BIGSERIAL`.

2. **Строковые типы:**
   - **Фиксированные строки:** `CHAR(n)`.
   - **Переменные строки:** `VARCHAR(n)`, `TEXT`.

3. **Дата и время:**
   - **Дата:** `DATE`.
   - **Время:** `TIME`, `TIME WITH TIME ZONE`.
   - **Дата и время:** `TIMESTAMP`, `TIMESTAMP WITH TIME ZONE`.
   - **Интервал:** `INTERVAL`.

4. **Логические типы:**
   - `BOOLEAN`.

5. **Бинарные типы:**
   - `BYTEA`.

6. **Геометрические типы:**
   - `POINT`, `LINE`, `LSEG`, `BOX`, `PATH`, `POLYGON`, `CIRCLE`.

7. **Сетевые типы:**
   - `INET`, `CIDR`, `MACADDR`.

8. **Перечисления:**
   - `ENUM`.

9. **Массивы:**
   - Поддерживаются массивы любого типа данных.

10. **JSON и XML:**
    - `JSON`, `JSONB`, `XML`.

11. **UUID:**
    - `UUID`.

12. **Составные типы:**
    - `COMPOSITE`.

13. **Домены:**
    - Пользовательские типы данных на основе существующих типов.

14. **Range типы:**
    - `INT4RANGE`, `INT8RANGE`, `NUMRANGE`, `TSRANGE`, `TSTZRANGE`, `DATERANGE`.

15. **Типы для хранения IP-адресов:**
    - `INET`, `CIDR`.

16. **Типы для хранения MAC-адресов:**
    - `MACADDR`.

17. **Типы для хранения геометрических объектов:**
    - `GEOMETRY`, `GEOGRAPHY` (через расширение PostGIS).
список команд для консоли PostgreSQL, которые пишутся через \:


 1. \l - список всех баз данных на сервере.
 2. \c - подключение к базе данных.
 3. \d - список всех таблиц в текущей базе данных.
 4. \dt - список всех таблиц в текущей базе данных с дополнительной информацией.
 5. \dv - список всех представлений в текущей базе данных.
 6. \di - список всех индексов в текущей базе данных.
 7. \ds - список всех последовательностей в текущей базе данных.
 8. \dT - список всех типов данных в текущей базе данных.
 9. \df - список всех функций в текущей базе данных.
 10. \dp - список всех прав доступа в текущей базе данных.
 11. \du - список всех пользователей в текущей базе данных.
 12. \dg - список всех групп в текущей базе данных.
 13. \dl - список всех языков программирования в текущей базе данных.
 14. \dn - список всех схем в текущей базе данных.
 15. \do - список всех операторов в текущей базе данных.
 16. \dp - список всех прав доступа в текущей базе данных.
 17. \dS - список всех системных таблиц в текущей базе данных.
 18. \dC - список всех системных каталогов в текущей базе данных.
 19. \dD - список всех системных доменов в текущей базе данных.
 20. \dT - список всех системных типов данных в текущей базе данных.

Некоторые другие команды:

 • \q - выход из консоли PostgreSQL.
 • \! - выполнение команды операционной системы.
 • \i - выполнение файла SQL.
 • \o - вывод результата запроса в файл.
 • \r - повторное выполнение последнего запроса.
 • \s - вывод истории запросов.
 • \t - вывод текущей таблицы.
 • \w - вывод текущей базы данных.


### Основные команды PostgreSQL

1. Создание базы данных
-- Создание новой базы данных
CREATE DATABASE mydatabase;
```

 2. Удаление базы данных
-- Удаление существующей базы данных
DROP DATABASE mydatabase;
```

 3. Создание таблицы
-- Создание таблицы с несколькими столбцами
CREATE TABLE employees (
    employee_id SERIAL PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    birth_date DATE,
    hire_date DATE
);
```

4. Удаление таблицы
-- Удаление существующей таблицы
DROP TABLE employees;
```

 5. Вставка данных
-- Вставка одной строки данных
INSERT INTO employees (first_name, last_name, birth_date, hire_date)
VALUES ('John', 'Doe', '1980-01-01', '2020-01-01');

-- Вставка нескольких строк данных
INSERT INTO employees (first_name, last_name, birth_date, hire_date)
VALUES 
('Jane', 'Doe', '1985-02-02', '2020-02-02'),
('Alice', 'Smith', '1990-03-03', '2020-03-03');
```

 6. Обновление данных
-- Обновление данных в таблице
UPDATE employees
SET first_name = 'Johnny'
WHERE employee_id = 1;
```

7. Удаление данных
-- Удаление строки данных из таблицы
DELETE FROM employees
WHERE employee_id = 1;
```

8. Выборка данных
-- Выборка всех данных из таблицы
SELECT * FROM employees;

-- Выборка данных с условием
SELECT * FROM employees
WHERE hire_date > '2020-01-01';

-- Выборка данных с сортировкой
SELECT * FROM employees
ORDER BY hire_date DESC;

-- Выборка данных Выберем всех «производителей»:
SELECT DISTINCT Manufacturer FROM Products;

Сортировка по одному столбцу в порядке возрастания:  SELECT * FROM employees
		ORDER BY hire_date ASC; 
Сортировка по одному столбцу в порядке убывания:  SELECT * FROM employees
		ORDER BY hire_date DESC;
Сортировка по нескольким столбцам:  SELECT * FROM employees
		ORDER BY hire_date DESC, salary ASC; 
Сортировка с условием:  SELECT * FROM employees
		WHERE hire_date > '2020-01-01'
		ORDER BY hire_date DESC; 
Сортировка с использованием алиасов: sSELECT first_name AS name, last_name AS surname FROM employees
		ORDER BY name ASC; 
Сортировка с использованием вычисляемых столбцов:  SELECT first_name, last_name, hire_date, salary, salary * 0.1 AS bonus FROM employees
		ORDER BY bonus DESC; 
Сортировка с использованием функций:  SELECT first_name, last_name, hire_date FROM employees
		ORDER BY LENGTH(first_name) ASC; 
Сортировка с использованием NULL значений: SELECT * FROM employees
		ORDER BY commission_pct NULLS FIRST; 
Сортировка с использованием NULL значений в конце:SELECT * FROM employees
		ORDER BY commission_pct NULLS LAST; 
Сортировка с использованием CASE: SELECT * FROM employees
		ORDER BY CASE 
		            WHEN hire_date > '2020-01-01' THEN 1
		            ELSE 2
		        END;

9. Создание индекса
-- Создание индекса на столбец
CREATE INDEX idx_employees_last_name
ON employees (last_name);
```

10. Удаление индекса
-- Удаление существующего индекса
DROP INDEX idx_employees_last_name;
```

11. Создание ограничений
-- Создание первичного ключа
ALTER TABLE employees
ADD CONSTRAINT pk_employees PRIMARY KEY (employee_id);

-- Создание внешнего ключа
CREATE TABLE departments (
    department_id SERIAL PRIMARY KEY,
    department_name VARCHAR(50)
);

ALTER TABLE employees
ADD COLUMN department_id INTEGER;

ALTER TABLE employees
ADD CONSTRAINT fk_employees_departments
FOREIGN KEY (department_id) REFERENCES departments(department_id);
```

12. Удаление ограничений
-- Удаление первичного ключа
ALTER TABLE employees
DROP CONSTRAINT pk_employees;

-- Удаление внешнего ключа
ALTER TABLE employees
DROP CONSTRAINT fk_employees_departments;
```

13. Группировка и агрегатные функции
-- Группировка данных и подсчет количества сотрудников в каждом департаменте
SELECT department_id, COUNT(*) AS employee_count
FROM employees
GROUP BY department_id;

-- Использование агрегатных функций
SELECT MAX(hire_date) AS latest_hire_date, MIN(hire_date) AS earliest_hire_date
FROM employees;
```

14. Подзапросы
-- Использование подзапроса для выборки данных
SELECT * FROM employees
WHERE department_id = (SELECT department_id FROM departments WHERE department_name = 'Sales');
```

15. Объединение таблиц
-- Внутреннее объединение таблиц
SELECT employees.first_name, employees.last_name, departments.department_name
FROM employees
INNER JOIN departments ON employees.department_id = departments.department_id;

-- Левое внешнее объединение таблиц
SELECT employees.first_name, employees.last_name, departments.department_name
FROM employees
LEFT JOIN departments ON employees.department_id = departments.department_id;
```

16. Транзакции
-- Начало транзакции
BEGIN;

-- Выполнение операций внутри транзакции
UPDATE employees
SET first_name = 'John'
WHERE employee_id = 1;

-- Фиксация транзакции
COMMIT;

-- Откат транзакции
ROLLBACK;
```

17. Пользователи и роли
-- Создание нового пользователя
CREATE USER myuser WITH PASSWORD 'mypassword';

-- Создание новой роли
CREATE ROLE myrole;

-- Назначение роли пользователю
GRANT myrole TO myuser;

-- Предоставление прав доступа к базе данных
GRANT ALL PRIVILEGES ON DATABASE mydatabase TO myuser;

-- Удаление пользователя
DROP USER myuser;

-- Удаление роли
DROP ROLE myrole;
```

18. Резервное копирование и восстановление
# Резервное копирование базы данных
pg_dump mydatabase > mydatabase_backup.sql

# Восстановление базы данных из резервной копии
psql mydatabase < mydatabase_backup.sql
```

19. Настройка параметров
-- Просмотр текущих параметров
SHOW all;

-- Изменение параметра
ALTER SYSTEM SET work_mem = '64MB';

-- Применение изменений
SELECT pg_reload_conf();
```

20. Работа с датами и временем
-- Выборка текущей даты и времени
SELECT NOW();

-- Форматирование даты и времени
SELECT TO_CHAR(NOW(), 'YYYY-MM-DD HH24:MI:SS');

-- Вычисление разницы между датами
SELECT AGE('2020-01-01', '2019-01-01');
```

Этот список основных команд и примеров поможет вам начать работу с PostgreSQL. Для более сложных задач и оптимизации запросов рекомендуется изучить документацию и дополнительные ресурсы по PostgreSQL.

На основе шаблона по PostgreSQL я подготовил более подробную шпаргалку для разработки с использованием Go (Golang) с примерами и комментариями.
￼
Шпаргалка для работы с PostgreSQL в Go с использованием драйвера `pgx` (v4 или v5) будет выглядеть следующим образом:

### Основные команды Go для работы с PostgreSQL (pgx)

1. Установка и подключение к базе данных
import (
    "context"
    "log"

    "github.com/jackc/pgx/v5"
    "github.com/jackc/pgx/v5/pgxpool"
)

func main() {
    connStr := "user=username dbname=mydatabase sslmode=disable"
    ctx := context.Background()

    // Подключение к базе данных PostgreSQL
    db, err := pgxpool.New(ctx, connStr)
    if err != nil {
        log.Fatal(err)
    }
    defer db.Close()
}

2. Создание базы данных
func createDatabase(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "CREATE DATABASE mydatabase")
    if err != nil {
        log.Fatal(err)
    }
}

3. Удаление базы данных
func dropDatabase(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "DROP DATABASE mydatabase")
    if err != nil {
        log.Fatal(err)
    }
}

4. Создание таблицы
func createTable(db *pgxpool.Pool, ctx context.Context) {
    query := `
    CREATE TABLE employees (
        employee_id SERIAL PRIMARY KEY,
        first_name VARCHAR(50),
        last_name VARCHAR(50),
        birth_date DATE,
        hire_date DATE
    );`
    _, err := db.Exec(ctx, query)
    if err != nil {
        log.Fatal(err)
    }
}

5. Удаление таблицы
func dropTable(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "DROP TABLE employees")
    if err != nil {
        log.Fatal(err)
    }
}
```

6. Вставка данных в таблицу
func insertData(db *pgxpool.Pool, ctx context.Context) {
    query := `
    INSERT INTO employees (first_name, last_name, birth_date, hire_date)
    VALUES ('John', 'Doe', '1980-01-01', '2020-01-01'),
           ('Jane', 'Doe', '1985-02-02', '2020-02-02'),
           ('Alice', 'Smith', '1990-03-03', '2020-03-03');`
    _, err := db.Exec(ctx, query)
    if err != nil {
        log.Fatal(err)
    }
}

 7. Обновление данных в таблице
func updateData(db *pgxpool.Pool, ctx context.Context) {
    query := `
    UPDATE employees
    SET first_name = 'Johnny'
    WHERE employee_id = 1;`
    _, err := db.Exec(ctx, query)
    if err != nil {
        log.Fatal(err)
    }
}

8. Удаление данных из таблицы
func deleteData(db *pgxpool.Pool, ctx context.Context) {
    query := `
    DELETE FROM employees
    WHERE employee_id = 1;`
    _, err := db.Exec(ctx, query)
    if err != nil {
        log.Fatal(err)
    }
}

9. Выборка данных из таблицы
func selectData(db *pgxpool.Pool, ctx context.Context) {
    rows, err := db.Query(ctx, "SELECT * FROM employees")
    if err != nil {
        log.Fatal(err)
    }
    defer rows.Close()

    for rows.Next() {
        var employee_id int
        var first_name, last_name string
        var birth_date, hire_date string
        err = rows.Scan(&employee_id, &first_name, &last_name, &birth_date, &hire_date)
        if err != nil {
            log.Fatal(err)
        }
        log.Println(employee_id, first_name, last_name, birth_date, hire_date)
    }
    err = rows.Err()
    if err != nil {
        log.Fatal(err)
    }
}

10. Добавление нового столбца
func addColumn(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, `ALTER TABLE employees ADD COLUMN phone VARCHAR(20) NULL`)
    if err != nil {
        log.Fatal(err)
    }
}
```

11. Удаление столбца
func dropColumn(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, `ALTER TABLE employees DROP COLUMN address`)
    if err != nil {
        log.Fatal(err)
    }
}

12. Изменение типа столбца
func alterColumnType(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, `ALTER TABLE employees ALTER COLUMN first_name TYPE VARCHAR(50)`)
    if err != nil {
        log.Fatal(err)
    }
}

13. Изменение ограничений столбца
func alterColumnConstraint(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, `ALTER TABLE employees ALTER COLUMN first_name SET NOT NULL`)
    if err != nil {
        log.Fatal(err)
    }

    _, err = db.Exec(ctx, `ALTER TABLE employees ALTER COLUMN first_name DROP NOT NULL`)
    if err != nil {
        log.Fatal(err)
    }
}

14. Изменение ограничений таблицы
func alterTableConstraint(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, `ALTER TABLE employees ADD CHECK (age > 0)`)
    if err != nil {
        log.Fatal(err)
    }

    _, err = db.Exec(ctx, `ALTER TABLE employees ADD PRIMARY KEY (employee_id)`)
    if err != nil {
        log.Fatal(err)
    }

    _, err = db.Exec(ctx, `ALTER TABLE employees ADD UNIQUE (email)`)
    if err != nil {
        log.Fatal(err)
    }

    _, err = db.Exec(ctx, `ALTER TABLE employees ADD CONSTRAINT phone_unique UNIQUE (phone)`)
    if err != nil {
        log.Fatal(err)
    }

    _, err = db.Exec(ctx, `ALTER TABLE employees DROP CONSTRAINT phone_unique`)
    if err != nil {
        log.Fatal(err)
    }
}
```

15. Переименование столбца и таблицы
func renameColumnAndTable(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, `ALTER TABLE employees RENAME COLUMN address TO city`)
    if err != nil {
        log.Fatal(err)
    }

    _, err = db.Exec(ctx, `ALTER TABLE employees RENAME TO users`)
    if err != nil {
        log.Fatal(err)
    }
}

16. Создание индекса
func createIndex(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "CREATE INDEX idx_employees_last_name ON employees (last_name)")
    if err != nil {
        log.Fatal(err)
    }
}

 17. Удаление индекса
func dropIndex(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "DROP INDEX idx_employees_last_name")
    if err != nil {
        log.Fatal(err)
    }
}

18. Создание и удаление ограничений (Constraints)
func addPrimaryKey(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "ALTER TABLE employees ADD CONSTRAINT pk_employees PRIMARY KEY (employee_id)")
    if err != nil {
        log.Fatal(err)
    }
}

func dropPrimaryKey(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "ALTER TABLE employees DROP CONSTRAINT pk_employees")
    if err != nil {
        log.Fatal(err)
    }
}

func addForeignKey(db *pgxpool.Pool, ctx context.Context) {
    query := `
    ALTER TABLE employees
    ADD COLUMN department_id INTEGER,
    ADD CONSTRAINT fk_employees_departments FOREIGN KEY (department_id) REFERENCES departments(department_id);`
    _, err := db.Exec(ctx, query)
    if err != nil {
        log.Fatal(err)
    }
}

func dropForeignKey(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "ALTER TABLE employees DROP CONSTRAINT fk_employees_departments")
    if err != nil {
        log.Fatal(err)
    }
}

### Пример полного кода
package main

import (
    "context"
    "log"

    "github.com/jackc/pgx/v5"
    "github.com/jackc/pgx/v5/pgxpool"
)

func main() {
    connStr := "user=username dbname=mydatabase sslmode=disable"
    ctx := context.Background()

    db, err := pgxpool.New(ctx, connStr)
    if err != nil {
        log.Fatal(err)
    }
    defer db.Close()

    createDatabase(db, ctx)
    createTable(db, ctx)
    insertData(db, ctx)
    updateData(db, ctx)
    selectData(db, ctx)
    createIndex(db, ctx)
    addPrimaryKey(db, ctx)
    addForeignKey(db, ctx)
    dropForeignKey(db, ctx)
    dropPrimaryKey(db, ctx)
    dropIndex(db, ctx)
    dropTable(db, ctx)
    dropDatabase(db, ctx)
}

func createDatabase(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "CREATE DATABASE mydatabase")
    if err != nil {
        log.Fatal(err)
    }
}

func dropDatabase(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "DROP DATABASE mydatabase")
    if err != nil {
        log.Fatal(err)
    }
}

func createTable(db *pgxpool.Pool, ctx context.Context) {
    query := `
    CREATE TABLE employees (
        employee_id SERIAL PRIMARY KEY,
        first_name VARCHAR(50),
        last_name VARCHAR(50),
        birth_date DATE,
        hire_date DATE
    );`
    _, err := db.Exec(ctx, query)
    if err != nil {
        log.Fatal(err)
    }
}

func dropTable(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "DROP TABLE employees")
    if err != nil {
        log.Fatal(err)
    }
}

func insertData(db *pgxpool.Pool, ctx context.Context) {
    query := `
    INSERT INTO employees (first_name, last_name, birth_date, hire_date)
    VALUES ('John', 'Doe', '1980-01-01', '2020-01-01'),
           ('Jane', 'Doe', '1985-02-02', '2020-02-02'),
           ('Alice', 'Smith', '1990-03-03', '2020-03-03');`
    _, err := db.Exec(ctx, query)
    if err != nil {
        log.Fatal(err)
    }
}

func updateData(db *pgxpool.Pool, ctx context.Context) {
    query := `
    UPDATE employees
    SET first_name = 'Johnny'
    WHERE employee_id = 1;`
    _, err := db.Exec(ctx, query)
    if err != nil {
        log.Fatal(err)
    }
}

func selectData(db *pgxpool.Pool, ctx context.Context) {
    rows, err := db.Query(ctx, "SELECT * FROM employees")
    if err != nil {
        log.Fatal(err)
    }
    defer rows.Close()

    for rows.Next() {
        var employee_id int
        var first_name, last_name string
        var birth_date, hire_date string
        err = rows.Scan(&employee_id, &first_name, &last_name, &birth_date, &hire_date)
        if err != nil {
            log.Fatal(err)
        }
        log.Println(employee_id, first_name, last_name, birth_date, hire_date)
    }
    err = rows.Err()
    if err != nil {
        log.Fatal(err)
    }
}

func createIndex(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "CREATE INDEX idx_employees_last_name ON employees (last_name)")
    if err != nil {
        log.Fatal(err)
    }
}

func dropIndex(db *pgxpool.Pool, ctx context.Context) {
    _, err := db.Exec(ctx, "DROP INDEX idx_employees_last_name")
    if err != nil {
        log.Fatal(err)
    }
}

