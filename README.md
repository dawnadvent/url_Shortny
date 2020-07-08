# url_Shortny
简单防红短链接，短链接生成，短链接加密，短链接二维码，短链接API，短链接自定义后缀，二维码API，QQ内部自动替换至浏览器打开，自定义广告
前端：
简洁、优雅、反应灵敏的设计
创建URL
创建自定义短链URL后缀
密码保护的链接
链接统计
QQ内自动跳转至浏览器（默认不带需要本功能需在https://sssn.top/WoEsz下载）
小书签
复制和共享链接

后端：
删除网址
编辑网站设置
添加或编辑广告
分析
使用自定义CSS

安装前请提前设置好伪静态

安装
环境要求：PHP、Mysql、Nginx/Apache

伪静态设置
Apache，编辑.htaccess文件，将本地地址修改成自己的域名
RewriteEngine on 
RewriteRule ^about                about.php [L]
RewriteRule ^api-about            api-about.php [L]
RewriteRule ^contact              contact.php [L]
RewriteRule ^tos                  tos.php [L]
RewriteRule ^([^/.]+)/?$          link.php?id=$1 [L]
RewriteRule ^404                  404.php [L]
Options -Indexes
ErrorDocument 404 http://自己的域名/404
ErrorDocument 403 http://自己的域名/404

Nginx，将下面例子的域名改成自己的
rewrite ^/about /about.php last;
rewrite ^/api-about /api-about.php last;
rewrite ^/contact /contact.php last;
rewrite ^/tos /tos.php last;
rewrite ^/([^/.]+)/?$ /link.php?id=$1 last;
rewrite ^/404 /404.php last;
error_page 404 http://自己的域名/404;
error_page 403 http://自己的域名/404;

然后开始安装，由于伪静态问题，只能通过具体路径安装，链接如下：
#安装路径，记得修改下面域名地址

https://xxx/install/index.html

安装完成后，默认用户名和密码均为admin

注意：非常重要！！！！
安装好后登录管理面板>设置>常规>修改成你的域名>保存>前台即可正常显示（否则前台错位乱码）这一步非常重要，安装好后必须先设置自己的域名。

后台路径：https://xxx/admin/index.php

看演示站吧https://sssn.top/
