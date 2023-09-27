# SQL-Server
SQL Server Management Studio
##### Using SQL Server Management Studio ######

--> To run a query to select backup history on database called 'msdb', select the msdb database as below:
Type 1:
select * from backupset
Type 2:
Exec use msdb
The query will open msdb database, you can execute the following query to select backup history.
Select * from backupset

--> To remove your database from MS SQL Server, use drop databse command.
Type 1:
Drop database <your database name>
Type 2:
Connect to SQL Sever and right click the database you want to remove. Click delete command and next page click 'OK' to remove the database.

--> Creating Backups
Type 1:
Full Type:
Backup database <Your database name> to disk = '<Backup file location + file name>'
Differential type:
Backup database <Your databse name> to disk = '<Backup file location + file name>' with differential
Log Type:
Backup log <Your databse name> to disk = '<Backup file location + file name>'
Type 2:
Using SSMS
step 1: Connect to db and expand databases folder 
step 2: Right click on 'TestDB' databse and select tasks. Click Backup 
step 3: Select backup file and make sure to check destination path which is where the backup file will be created. 
step 4: Click OK to create 'TestDB' database full backup.

--> Restoring Databases
Type 1:
Restore databse <Your database name> from disk = '<Backup file location + file name>'
Type 2:
Using SSMS
step 1: Connect to db instance and right click on db's folder. Click restore db 
step 2: Select device radio button and click on ellipse to select the backup file
step 3: Click OK and pop up a screen
step 4: Select files option which is on the top left corner 
step 5: Select options which is on the top left corner and click OK to restore db.

--> Create Users
Type 1:
Create user<username> for login <loginname>
Type 2:
Uisng SSMS
step 1: connect SQL server and expand db's folder. Then expand db where we are going to create the user account and expand the security folder. Right click on users and click on the new user .
step 2: Enter nmae in the user name field and click on ellipse to select the login name .
step 3: Click OK to display login name.

--> Assign Permissions
Type 1:
Use <db name>
Grant <permission name> on <object name> to <username\principle>

Type 2:
Using SSMS
Step 1: Connect to instance and expand folders.
step 2: Right click on user and click properties.
step 3: Click search and select specific options. Click object types, select tables and click browse. Select 'TestTable' and Click OK.
step 4: Select checkbox for Grant column under select permission and click OK 
step 5:select permission on db granted to user. Click OK.

