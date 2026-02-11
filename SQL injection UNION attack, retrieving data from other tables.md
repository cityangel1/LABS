SQL injection UNION attack, retrieving data from other tables \
Goal -  The database contains a different table called users, with columns called username and password. \
       To solve the lab, perform a SQL injection UNION attack that retrieves all usernames and passwords, and use the information to log in as the administrator user. \
Step 1 - \
 try \
  ' UNION SELECT username,password FROM users --  \
  <img width="1602" height="908" alt="image" src="https://github.com/user-attachments/assets/28bddc24-d3b6-455b-9b32-7e0f8fa8dd96" /> \
  <img width="633" height="408" alt="image" src="https://github.com/user-attachments/assets/479b86ea-34a9-4780-a06e-2ed2a088af30" /> \
It all ends in Step 1 \
<img width="1919" height="853" alt="image" src="https://github.com/user-attachments/assets/daabc65c-6dc9-4d3c-b0cb-44a830ea2631" /> \
