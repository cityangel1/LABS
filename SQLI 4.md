SQL injection attack, querying the database type and version on Oracle
 This lab contains a SQL injection vulnerability in the product category filter. You can use a UNION attack to retrieve the results from an injected query.
<img width="955" height="926" alt="image" src="https://github.com/user-attachments/assets/d025b419-fb1d-4a41-a316-6fadccf4537f" />
<img width="808" height="263" alt="image" src="https://github.com/user-attachments/assets/bf1cc50c-ca32-4120-92c0-c9964b269f78" />

TRIED BURP PROXY.
<img width="1600" height="908" alt="image" src="https://github.com/user-attachments/assets/1520c189-8522-4285-b778-6646e0a43b61" />

first is to know the number of columns.=2
<img width="1599" height="901" alt="image" src="https://github.com/user-attachments/assets/b05666a7-b1ed-4f9b-b790-bb4c9f070524" />
That confirms it.its 2 columns.
Now.we need to know the datatype.BUt wait,we guess is string from the website.lets pretend to be dumb and confirm this.
<img width="1600" height="901" alt="image" src="https://github.com/user-attachments/assets/44a2f24a-f9e0-483e-bac5-cd2f2678fe27" />
No error means its string
NOW GET THE DATABASE INFO.
' UNION SELECT * FROM v$version-- = get oracle database information.
<img width="1598" height="908" alt="image" src="https://github.com/user-attachments/assets/11a7eee0-04fe-45a4-8aea-976205086970" />
it worked.Felt like a hero!!.
<img width="964" height="719" alt="image" src="https://github.com/user-attachments/assets/3f1bffe6-df6f-483f-a9ef-d54d048954d1" />

