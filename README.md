# Oracle-Tutorial-5---How-to-create-tablespace-without-autoextend-on-datafile-user-and-grant-permiss
Oracle Tutorial 5 - How to create tablespace without autoextend on, datafile, user and grant permission


Steps: ---
1. Login to your Oracle Database. (sqlplus / as sysdba)
2. run the below commands.

 Check the path of datafiles.
 SQL> select name from v$datafile;

 You ll get the location of datafiles. So i ll create new datafile in same location.
 Here chirag is tablespace name. and also user is chirag. Creating datafile with size 1 GB.
 SQL> CREATE TABLESPACE chirag DATAFILE 'D:\APP\CHIRAG\ORADATA\ORCL\chirag01.dbf' size 1G;

Tablespace created. Now creating user for tablespace.

 SQL> create user chirag identified by chirag default tablespace chirag;

User created. Now give the permission to user.
 SQL> grant dba to chirag;

Grant succeeded.

3. Now check in path that 'chirag01.dbf' file is created or not.
 Datafile is created with given size.
 
 Video URL : https://chittranjanmahto.blogspot.com/2019/08/oracle-tutorial-5-how-to-create.html
