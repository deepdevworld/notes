# SQL commands for postgres
***
* ***To select all the table which is present in the database which is in public: run `SELECT tablename FROM pg_catalog.pg_tables WHERE schemaname = 'ppublic';` where pg_catalog.pg_table stores the metadata 		information of the table in postgres database.***
* ***To select everything from the table run: `SELECT * FROM public."table_name";`***
* ***To select a particular data using id run: `SELECT column_name FROM public."table_name" WHERE id=the_id_for_which_you_want_data;`***
***
# MAIN COMMANDS
***
* ***To CREATE a table run: <br>`CREATE TABLE name_of_the_table (id SERIAL PRIMARY KEY, name varchar(255));`***
* ***To INSERT a values run: <br>`INSERT INTO table_name (column_name) VALUES(value_for_that_column);`***
* ***To ALTER the column run: <br>`ALTER TABLE table_name ALTER COLUMN column_name SET data_type;`***
* ***To ADD new column to the existing column run: <br>`ALTER TABLE table_name ADD COLUMN column_name data_type;`***
* ***To UPDATE the value in the table using id run: <br>`UPDATE table_name SET column_name = value WHERE id=selected_id;`***
* ***To DELETE the table run: <br>`DROP TABLE table_name;`***
* ***To ignore duplicate rows in query run: <br>`SELECT DISTINCT column_name FROM table_name;`***
* ***To JOIN the two tables with id run:<br>`SELECT * FROM table_name a JOIN table_name2 b WHERE a.id=b.id;` here, both the table has id so to avoid the error a and b also called table alies is used to refrence to the table_name we can also use `SELECT * FROM table_name JOIN table_name2 WHERE table_name.id=table_name2.id;`.***
* ***The JOIN of two table in other format run: `SELECT * FROM table1, table2 WHERE table1.id=table2.id;`***
* ***To create VIEW***
  * ```sql
    CREATE VIEW myview AS SELECT notes.title, notes.data, users.name, users.email FROM notes, users WHERE users.id = notes.id;
    ```
