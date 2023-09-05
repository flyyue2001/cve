There is a backend SQL injection vulnerability in the D-LINK DAR-7000 series online behavior audit gateway. Attackers can exploit vulnerabilities to gain server privileges or cause business impact on the system.

official： http://www.dlink.com.cn/

version:DAR-7000

 Vulnerability Path  ：/useratte/editwebuser.php![image](https://github.com/flyyue2001/cve/assets/88701694/09f7da57-6915-4334-bdc6-71f3016df44f)


See the login page.

https://60.22.74.195:8443/

<img width="730" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/96abc24b-20b8-41be-94ab-93f545830440">



There is a default account password present： test/admin@123



<img width="725" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/9563a5dc-605b-4b80-af22-54c28f4cdc10">



​                               

 Construct the following POC to determine the presence of SQL injection for the id parameter  

POC：

GET /useratte/editwebuser.php?id=(select*from(select(sleep(3)))a) HTTP/1.1
![image](https://github.com/flyyue2001/cve/assets/88701694/a280a5d4-1606-4dcb-b040-cd5d914d68e8)


<img width="723" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/264c217c-38c8-4b8b-a304-0fe4f512e02a">


 By analogy, obtain the database name nsg    

<img width="726" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/a0b78d24-c3e9-4985-a634-feb2ed714c7d">


 
