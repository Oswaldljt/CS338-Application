# CS338-Application

1. Introduction:
   This README file provides instructions on how to create and load a sample database onto your chosen platform using MySQL and PHP. It is intended for use by team members and anyone interested in replicating the database setup.

2. Requirements:
   - MySQL installed on your local computer.
   - PHP installed and configured on your local computer.

3. Steps to Create and Load the Sample Database:
   Step 1: Install MySQL:
      a. Download and install MySQL on your computer. Instructions can be found at https://dev.mysql.com/doc/refman/8.0/en/installing.html.
      b. After installing MySQL, create a database named 'testDB' and a user with appropriate permissions. For example:
         ```
         $ mysql -u root -p (or sudo mysql -u root)
         mysql> CREATE DATABASE testDB;
         mysql> CREATE USER 'sujaya'@'localhost' IDENTIFIED BY 'Password0!';
         mysql> GRANT ALL ON testDB.* TO 'sujaya'@'localhost';
         mysql> ALTER USER 'sujaya'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Password0!';
         ```
   Step 2: Install and Configure PHP:
      a. Download, install, and configure PHP on your local computer. Instructions can be found at https://www.php.net/docs.php.
      b. For example, if you are using MacOS, you can start PHP with the command:
         ```
         $ php -S 127.0.0.1:8000
         ```
   Step 3: Create Table and Insert Data:
      a. Once MySQL and PHP are set up, you can create a table and insert sample data. For example:
         ```
         $ mysql -u root -p (or sudo mysql -u root)
         mysql> USE testDB;
         mysql> CREATE TABLE student(uid DECIMAL(3, 0) NOT NULL PRIMARY KEY, name VARCHAR(30), score DECIMAL(3, 2));
         mysql> INSERT INTO student VALUES(1, 'alice', 0.1);
         mysql> INSERT INTO student VALUES(2, 'bob', 0.4);
         ```
4. Testing:
   - After completing the setup, you can run a PHP script (e.g., testDB.php) to test the connection and display query results in the browser. 
   - Type "http://127.0.0.1:8000/testDB.php" in your browser to see the message "2 students in the student table" if the setup is successful.
