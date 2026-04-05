#Notes 3

*Normalization*
 - Breaking data into multiple tables reduces redundancy and improves consistency.
*Relationships*
 - Using foreign keys, we linked meals with their ingredients. This allows for more meaningful data retrieval.
*Querying*
 - We practiced SELECT, JOIN, WHERE, ORDER BY, and GROUP BY to manipulate and filter data results.
*Management*
 - We reviewed how to create a database, grant privileges to the database to a specific user, remove those privileges, and delete the database.

#Apache2
 - The benefit of Apache2 having a user is that we can limit file permissions and ownership to this user.
 - The general guidelines for this are as follows:
    - Static files (like HTML, CSS, JS) might not need to be writable by the Apache server, so they could be owned by a different user (like your own user account) but be readable by www-data.
    - Directories where Apache needs to write data (like upload directories) or applications that need write access should be owned by www-data.
    - Configuration files (incl. files like login.php) should be readable by www-data but not writable, to prevent unauthorized modifications.

