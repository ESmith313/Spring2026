# Spring2026
This repository was created for LIS624 during the 2026 Spring semester. It will serve as the main documentation space for my work throughout the semester.

**What this repository will contain:**
 - Notes from lectures and readings.
 - Assignment documentation.
 - Reflections.

**What has been set up:**
 - Public GitHub repository.
 - Added and edited this README file using Markdown.
 - Connected GitHub to my Virtual Machine.


## LAMP Stack Server Setup

**Introduction:**
 - A LAMP Stack consists of Linux, Apache, MySQL, and PHP. It is used to host dynamic web applications by combining a web server, database, and server-side scripting language.

**Apache Installation:**
 *sudo apt update*
 *sudo apt install apache2 -y*
 - I verified Apache was running using:
 *systemctl status apache2*
 - I then tested it was working by visiting my VM's public IP address.
**PHP Installation:**
 *sudo apt install php libapache2-mod-php php-mysql -y*
 - I restarted Apache:
 *sudo systemctl restart apache2*
 - I confirmed PHP worked using an info.php file.
 - Configeration Changes:
   - I edited the Apache configeration file (dir.conf) to prioritize index.php over index.html.
   *DirectoryIndex index.php index.html*
 - index.php Page:
   - I created an index.php file that detects the user's browser and operating system using PHP variables and conditional statements.
**MySQL Installation:**
 *sudo apt install mysql-server -y*
 *sudo mysql_secure_installation*

**I Created:**
 - Database: opacdb
 - User: opacuser
 - Table: books

**OPAC Page**
 - I created opac.php, which connects to the MySQL database and displays book records from the books table.

**Verification:**
 - I accessed index.php in the browser.
 - I accessed opac.php and confirmed database data was displayed.
 - I checked Apache and MySQL status.

**Challenges:**
 - Other than mistyping some commands my biggest challenge was when my VM stopped working and I had to set up a new one and redo some of the coursework.


## OPAC and Cataloging Module Documentation

**Introduction**
 - An OPAC (Online Public Access Catalog) is the part of a library system that allows users to search for and view materials such as books, media, and other resources. It acts as the public-facing interface of a larger Integrated Library System (ILS). Instead of interacting directly with a database, users interact with the OPAC, which retrieves and displays information in a readable format.
 - The cataloging module works on the backend of the system and is used to create and manage bibliographic records. These records include information such as titles, authors, and other descriptive details. Together, the cataloging module and OPAC form a simple workflow where data is entered, stored in a database, and then retrieved for user searches.

**Relational Database Structure**
 - The system uses a relational database to store bibliographic records. In a relational database, data is organized into tables made up of rows and columns. Each row represents a single record (such as a book), and each column represents a specific field (such as title or author).
 - Each table includes a primary key, which uniquely identifies each record. This helps prevent duplicate entries and allows the system to efficiently locate specific records. Fields are assigned data types such as `INT` for numerical values and `VARCHAR` for text.
 - The OPAC interacts with this database by sending queries to retrieve records based on user input. This structure allows for efficient storage, organization, and retrieval of information.

**Step-by-Step Setup**
 - Database Connection
   - The system connects to the database using PHP. This requires specifying the database host, username, password, and database name. If any of these values are incorrect, the connection will fail and the system will not function.
   - Once connected, PHP can send queries to the database to insert or retrieve data.
 - Cataloging Module
   - The cataloging module allows users to add new records to the database. It typically includes a form where users input information such as title and author.
   - When the form is submitted, the data is sent to the database using an SQL `INSERT` statement. This adds a new row to the table, making the record available for retrieval in the OPAC.
 - OPAC Search and Retrieval
   - The OPAC allows users to search for records stored in the database. When a user enters a search term, the system sends an SQL `SELECT` query to the database.
   - The database returns any matching records, which are then displayed on the page. This demonstrates how the frontend (user interface) interacts with the backend (database).
 - Making the System More Realistic
   - The system created in this assignment is a basic version of a library system. In real-world applications, additional features would be included, such as:
     - User accounts and authentication
     - Circulation systems for checking items in and out 
     - Subject headings and classification systems
     - Advanced search functionality
   - Adding these features would make the system more similar to a full Integrated Library System.
 - Configuration
   - The system runs on a LAMP stack, which includes Linux (Ubuntu), Apache, MySQL, and PHP. Setting up the environment requires installing these components and ensuring they are properly configured.
 - The server must be running, and all dependencies must be installed for the OPAC and cataloging modules to function correctly. Misconfigurations or missing components can prevent the system from working.

**Key Details**
 - Small details are critical to making the system function properly. This includes correct data types, proper SQL syntax, and consistent naming conventions.
 - For example, forgetting a semicolon or misspelling a variable name can cause errors that prevent the program from running. Ensuring that database fields match expected data types is also important for avoiding issues when inserting or retrieving data.
 - These small but important details highlight the need for precision when working with databases and programming.

**Using Documentation**
 - Documentation played an important role in understanding how the system works. While working with PHP and SQL, it was often necessary to refer to documentation and examples to understand how to properly structure code and queries.
 - In some cases, the provided materials did not fully explain certain steps, so additional resources and troubleshooting were needed. This included looking up syntax, reviewing examples, and testing different approaches to fix errors.
 - Using documentation and external resources helped fill in gaps in understanding and made it possible to complete the assignment successfully.

---
# OPAC
**Link:** http://34.9.67.253/opac.php

# Cataloging Module
**Link:** http://34.9.67.253/cataloging/index.html

# Login Credentials
**Username:** libcat
**Password:** password123
