04.29 06:25
termux笔记3能在手机存储里直接查看的文件夹只有这几个

第一步安装php

安装PHP

Termux 官方封装了 PHP，所以我们安装起来就很方便：

pkg install php

安装完成后查看下版本信息：

php --version

自 PHP5.4 之后 PHP内置了一个 Web 服务器。在 Termux 下可以很方便地测试 PHP 文件

安装php后无需绑定任何组件，

直接创建目录创建文件，启动 WebServer后直接访问即可，http://127.0.0.1:8888


开启本地访问权限

termux-setup-storage


mkdir ~/    (在家目录下创建新文件夹)


mkdir ~/www(在家目录下创建www文件夹)

mkdir ~/storage(家目录下的手机存储文件夹)

mkdir ~/xxx家目录下创建的新文件夹

是隐藏的目录

mkdir ~/   家目录下的 文件夹  和家目录mkdir ~/storage   是同同级目录  是隐藏的目录

手机存储里是不能直接查看，包括用es都不能直接查看，
————————————
在手机存储里

能直接查看的文件夹只有这几个

ls storage


dcim       movies   pictures  
downloads  music   shared

不用创建，本地手机存储里就有，的文件夹

mkdir ~/storage/dcim

mkdir ~/storage/movies

mkdir ~/storage/pictures

mkdir ~/storage/downloads

mkdir ~/storage/music

mkdir ~/storage/shared

dcim       movies   pictures  
downloads  music   shared

不用创建，本地手机存储里就有，的文件夹

——————————————

mkdir ~/    (在家目录下创建新文件夹)

mkdir ~/xxx家目录下的文件夹

不能直接查看，包括用es都不能直接查看

mkdir ~/storage/家目录下storage目录下创建的新文件夹

都不能直接查看，包括用es都不能直接查看，

——————————

Welcome to Termux!

Community forum: https://termux.com/community
Gitter chat:     https://gitter.im/termux/termux
IRC channel:     #termux on freenode

Working with packages:

 * Search packages:   pkg search <query>
 * Install a package: pkg install <package>
 * Upgrade packages:  pkg upgrade

Subscribing to additional repositories:

 * Root:     pkg install root-repo
 * Unstable: pkg install unstable-repo
 * X11:      pkg install x11-repo

Report issues at https://termux.com/issues

The Google Play version of the Termux app no longer
receives updates. For more information, visit:
https://wiki.termux.com/wiki/Termux_Google_Play

~ $ cd

~ $ mkdir ~/www

~ $ mkdir ~/www2

~ $ ls

storage   www   www2

~ $ ls storage
dcim       movies  pictures  www
downloads  music   shared

~ $ mkdir ~/storage/downloads/www3


~ $ ls storage/dcim     错误的查看方法
Camera  Notes  Screenshots
~ $ ls dcim
ls: cannot access 'dcim': No such file or directory
~ $ cd dcim

bash: cd: dcim: No such file or directory

~ $ ls storage/dcim/     正确的查看方法

Camera  Notes  Screenshots


~ $ ls storage/dcim/camera/
IMG_20210428_085002.jpg
IMG_20210428_154137.jpg
video_20210428_130322.mp4
video_20210428_130728.mp4

————————
~ $ ls storage/dcim/         正确的查看方法
12.txt  8.php  99.txt    Notes        index.php
8.html  8.txt  Camera  Screenshots   ww


~ $ ls -a
.  ..  .termux  .viminfo  storage  www  www2
~ $ ls -a www
.  ..  1.txt  index.php
~ $ ls -a .viminfo
.viminfo
~ $ ls -a .  ..  .termux
.:
.  ..  .termux  .viminfo  storage  www  www2

..:
.  ..  home  usr

.termux:
.  ..  termux.properties
~ $



echo '' > ~/storage/www/index.php

php -S 0.0.0.0:8888 -t   storage/www/

————————

创建后在手机存储里能直接查看

echo '' > ~/storage/dcim/index.php


php -S 0.0.0.0:8888 -t   storage/dcim/


echo '' > ~/storage/dcim/ww/9.txt



php -S 0.0.0.0:8888 -t   storage/dcim/



重启服务器
php -S 0.0.0.0:8888 -t   storage/dcim/

创建后在手机存储里能直接查看


用浏览器访问

http://127.0.0.1:8888/

http://127.0.0.1:8888/storage/dcim/



——————————

长按屏幕

more

kill  process(29423)

关闭进程

关闭窗口进程

——————
