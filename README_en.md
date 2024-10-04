# MySQL Database Automatic Configuration Script 🚀

This script helps to create a MySQL database, add tables, and columns interactively. It is designed to be used with the MySQL connector for Python (`mysql-connector-python`).

## Prerequisites 📋

-   Python 3.x
-   The MySQL connector for Python (`mysql-connector-python`)

You can install the MySQL connector using pip:

```sh
pip install mysql-connector-python
```

## Usage 🛠️

1. **Running the script:**
   Run the script using Python:

    ```sh
    python main_fr.py
    python main.py
    ```

    Depending on your preference, choose `main.py` for English and `main_fr.py` for French.

2. **Database Connection**:
   The script will prompt you to enter the connection information for the MySQL database (username, password, host).

3. **List Databases**:
   You will have the option to list existing databases on the MySQL server.

4. **Create Database**:
   The script will prompt you to enter the name of the database to create. If the database already exists, it will be used.

5. **List Tables**:
   You will have the option to list existing tables in the selected database.

6. **Create Table**:
   The script will prompt you to enter the name of the table to create. An `id` column with auto-increment will be added as the primary key.

7. **Add Columns**:
   You can add as many columns as you want to the table. The script supports the following column types:

    - `VARCHAR`: You will be prompted to enter the length of the column.
    - `BOOLEAN`: You will be prompted to enter the default value of the column.
    - `INT`, `FLOAT`, `TIMESTAMP`: These types are accepted directly without additional input.
        > (The program does not support more values to avoid unnecessary errors.)

8. **Closing the connection**:
   Once all operations are completed, the connection to the database will be closed automatically.

## Example Output 📄

```sh
Do you want to list the databases? (y/n): y
# List of databases:
> database1
> database2

Enter the name of the database: testdb
# Database created successfully!

Do you want to list the tables? (y/n): y
# List of tables:
> table1
> table2

Enter the name of the table: users
# Table created successfully!
# Column id added with auto-increment as primary key

Do you want to add another column? (y/n): y
Enter the name of the column: name
Enter the type of the column (VARCHAR, BOOLEAN, INT, FLOAT, TIMESTAMP): VARCHAR
Enter the length of the column: 255
# Column name:VARCHAR(255) created successfully!

Do you want to add another column? (y/n): n
# Connection to the database closed successfully!
```

## Warnings ⚠️

-   This script will overwrite any existing database with the same name. Make sure to back up your data before running this script.
-   The script is designed to be used in a development environment. Use it with caution in a production environment.

## Author 👤

-   NEY_Twix

## License 📜

This project is licensed under the MIT License. See the [`LICENSE`](https://github.com/NeyTwix/SQL-Auto-Setup/blob/main/LICENSE "LICENSE") file for more details.
