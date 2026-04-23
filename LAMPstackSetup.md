## LAMP Stack Server Setup

**Introduction:**
 - A LAMP Stack consists of Linux, Apache, MySQL, and PHP. It is used to host dynamic web applications by combining a web server, database, and server-side>

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
