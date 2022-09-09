
# MySQL information

## Queries

- Getting ForeignKeys for a Table
    ``` sql
    -- FOR A TABLE
    SELECT 
    TABLE_NAME,COLUMN_NAME,CONSTRAINT_NAME, REFERENCED_TABLE_NAME,REFERENCED_COLUMN_NAME
    FROM
    INFORMATION_SCHEMA.KEY_COLUMN_USAGE
    WHERE
    REFERENCED_TABLE_SCHEMA = '<database>' AND
    REFERENCED_TABLE_NAME = '<table>';
    ```
- Getting ForeignKeys for a Column
    ``` sql
    -- FOR A COLUMN
    SELECT 
    TABLE_NAME,COLUMN_NAME,CONSTRAINT_NAME, REFERENCED_TABLE_NAME,REFERENCED_COLUMN_NAME
    FROM
    INFORMATION_SCHEMA.KEY_COLUMN_USAGE
    WHERE
    REFERENCED_TABLE_SCHEMA = '<database>' AND
    REFERENCED_TABLE_NAME = '<table>' AND
    REFERENCED_COLUMN_NAME = '<column>';
    ```
- Getting MySQL Table information like a Create command
    ``` sql
    -- BASIC INFO
    SHOW CREATE TABLE '<table>';
    ```