# SQL Practical Exercises: Create Table

This repository contains a practical MySQL exercise for designing and managing a relational database for a company. The accompanying SQL script walks through table creation, table modification, table removal, constraints, and indexes for employees, departments, projects, and task assignments.

## Why this project is useful

- Provides a compact, hands-on introduction to relational database design.
- Demonstrates primary keys, foreign keys, uniqueness, and `NOT NULL` constraints.
- Shows how to evolve a schema with `ALTER TABLE`.
- Introduces temporary tables and conditional table deletion.
- Demonstrates single-column and composite indexes.
- Includes a written record of the exercise and observations in [`exercises.md`](exercises.md).

## Project contents

| Path | Description |
| --- | --- |
| [`f67mcxBQkqhz1g9iOGgz_Module_6/Module_6.sql`](f67mcxBQkqhz1g9iOGgz_Module_6/Module_6.sql) | Main MySQL exercise script |
| [`exercises.md`](exercises.md) | Exercise notes, alternative statements, and observations |
| `Practical@0020Exercises/` | Exported MySQL table files from the exercise database |
| [`f67mcxBQkqhz1g9iOGgz_Module_6.zip`](f67mcxBQkqhz1g9iOGgz_Module_6.zip) | Packaged copy of the module files |

## Getting started

### Prerequisites

- MySQL 8.0 or a compatible MySQL server
- A MySQL client, such as the `mysql` command-line client or DBeaver
- Permission to create and alter tables in a local practice database

### Set up a practice database

Create and select a disposable database before running the exercise:

```sql
CREATE DATABASE sql_practical_exercises;
USE sql_practical_exercises;
```

Run the script from the repository root with the MySQL client:

```bash
mysql -u YOUR_USERNAME -p sql_practical_exercises \
  < f67mcxBQkqhz1g9iOGgz_Module_6/Module_6.sql
```

The script is designed as a sequence of lessons. Read and run statements in order, preferably one lesson at a time:

1. Create `Employees`, `Departments`, and `Projects`.
2. Alter the tables to add, rename, and remove columns.
3. Practice dropping tables and creating a temporary table.
4. Create `TaskAssignments` and apply additional constraints.
5. Create and remove indexes.

The later lessons intentionally modify or drop objects created earlier. Use a disposable database and review each statement before executing it. The complete script is not intended to be safely rerun without resetting the database.

## Usage example

To inspect the schema after running the creation statements:

```sql
SHOW TABLES;
DESCRIBE Employees;
DESCRIBE Departments;
DESCRIBE Projects;
```

For the exercise prompts and the author's notes about alternate approaches, see [`exercises.md`](exercises.md).

## Getting help

Start with the comments in [`Module_6.sql`](f67mcxBQkqhz1g9iOGgz_Module_6/Module_6.sql) and the detailed notes in [`exercises.md`](exercises.md). If you find an issue or have a question that is not answered there, [open an issue](https://github.com/VoidLance/course-files-sql-practical-exercises-createtable/issues) with:

- the MySQL version and client you used;
- the lesson and statement involved;
- the exact error message; and
- the smallest reproducible example.

## Contributing

Contributions are welcome. To propose an improvement:

1. Fork the repository and create a focused branch.
2. Update the SQL or documentation while preserving the exercise's learning objectives.
3. Test SQL changes against a disposable MySQL database.
4. Open a pull request describing what changed and how it was tested.

Please avoid committing database credentials, generated secrets, or unrelated exported database files.

## Maintainer

This project is maintained by [VoidLance](https://github.com/VoidLance). Bug reports, corrections, and educational improvements are welcome through GitHub issues and pull requests.
