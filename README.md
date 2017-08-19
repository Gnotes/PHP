# PHP

## PHP是什么

PHP is a popular general-purpose scripting language that is especially suited to web development.     
PHP（“PHP: Hypertext Preprocessor”，超文本预处理器的字母缩写）是一种被广泛应用的开放源代码的多用途脚本语言，它可嵌入到 HTML中，尤其适合 web 开发

- PHP 是一种免费的创建动态交互性站点的强有力的服务器端脚本语言。
- 与客户端的`JavaScript` 不同的是，`PHP` 代码是运行在服务端的。如果在服务器上建立了如上例类似的代码，则在运行该脚本后，客户端就能接收到其结果，但他们无法得知其背后的代码是如何运作的

## PHP能做什么

- 服务端脚本 : 网站和 web 应用程序
- 命令行脚本
- 编写桌面应用程序

感觉上能做的挺多的，详细查看：[`PHP 能做什么?`](http://php.net/manual/zh/intro-whatcando.php)

## 安装

[Mac 安装](http://laravel-china.github.io/php-the-right-way/#mac_setup)
[(Re)Install php on Mac](http://justinhileman.info/article/reinstalling-php-on-mac-os-x/)

> Mac其实自带了php，但版本一般都比较低（我的是v5.6.30），使用brew 可以重新安装高版本的 `brew install php71` `71`为php的版本号

> **安装前**: 如果存在 ~/.pearrc, ~/.pear，你可以删除掉，因为他会阻止brew安装最新版本的pear,以及 /usr/local/lib/php 这个目录下的php

```
brew install php71 --with-apxs --with-gmp --with-imap --with-tidy --with-debug --with-phpdbg --with-httpd24
```

可选参数:

通过`brew options php71` 可查看当前版本安装的可选参数

```
--disable-opcache
    Build without Opcache extension
--disable-zend-multibyte
    Disable auto-detection of Unicode encoded scripts (PHP 5.2 and 5.3 only)
--homebrew-apxs
    Build against apxs in Homebrew prefix
--with-apache
    Enable building of shared Apache 2.0 Handler module, overriding any options which disable apache
--with-cgi
    Enable building of the CGI executable (implies --without-apache)
--with-debug
    Compile with debugging symbols
--with-fpm
    Enable building of the fpm SAPI executable (implies --without-apache)
--with-gmp
    Build with gmp support
--with-homebrew-curl
    Include Curl support via Homebrew
--with-homebrew-libxslt
    Include LibXSLT support via Homebrew
--with-homebrew-openssl
    Include OpenSSL support via Homebrew
--with-imap
    Include IMAP extension
--with-libmysql
    Include (old-style) libmysql support instead of mysqlnd
--with-mssql
    Include MSSQL-DB support
--with-pdo-oci
    Include Oracle databases (requries ORACLE_HOME be set)
--with-pgsql
    Include PostgreSQL support
--with-phpdbg
    Enable building of the phpdbg SAPI executable (PHP 5.4 and above)
    PHPDBG是一个PHP的SAPI模块，可以在不用修改代码和不影响性能的情况下控制PHP的运行环境。PHPDBG的目标是成为一个轻量级、强大、易用的PHP调试平台
--with-thread-safety
    Build with thread safety
--with-tidy
    Include Tidy support
--without-bz2
    Build without bz2 support
--without-mysql
    Remove MySQL/MariaDB support
--without-pcntl
    Build without Process Control support
--without-pear
    Build without PEAR
--HEAD
    install HEAD version
```

仔细阅读安装输出：

```
Updating Homebrew...
==> Installing php71 from homebrew/php
==> Installing dependencies for homebrew/php/php71: boost, spdylay, jemalloc, nghttp2, homebrew/apache/httpd24
==> Installing homebrew/php/php71 dependency: boost
==> Downloading https://homebrew.bintray.com/bottles/boost-1.64.0_1.sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring boost-1.64.0_1.sierra.bottle.tar.gz
🍺  /usr/local/Cellar/boost/1.64.0_1: 12,628 files, 395.7MB
==> Installing homebrew/php/php71 dependency: spdylay
==> Downloading https://homebrew.bintray.com/bottles/spdylay-1.4.0_1.sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring spdylay-1.4.0_1.sierra.bottle.tar.gz
🍺  /usr/local/Cellar/spdylay/1.4.0_1: 18 files, 837.8KB
==> Installing homebrew/php/php71 dependency: jemalloc
==> Downloading https://homebrew.bintray.com/bottles/jemalloc-5.0.1.sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring jemalloc-5.0.1.sierra.bottle.tar.gz
🍺  /usr/local/Cellar/jemalloc/5.0.1: 16 files, 1.6MB
==> Installing homebrew/php/php71 dependency: nghttp2
==> Downloading https://homebrew.bintray.com/bottles/nghttp2-1.25.0.sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring nghttp2-1.25.0.sierra.bottle.tar.gz
🍺  /usr/local/Cellar/nghttp2/1.25.0: 33 files, 5.9MB
==> Installing homebrew/php/php71 dependency: homebrew/apache/httpd24
==> Downloading https://homebrew.bintray.com/bottles-apache/httpd24-2.4.27.sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring httpd24-2.4.27.sierra.bottle.tar.gz
==> Caveats
To have launchd start homebrew/apache/httpd24 now and restart at login:
  brew services start homebrew/apache/httpd24
Or, if you don't want/need a background service you can just run:
  apachectl start
==> Summary
🍺  /usr/local/Cellar/httpd24/2.4.27: 1,624 files, 25.8MB

Warning: homebrew/php/php71: --with-apache was deprecated; using --with-httpd24 instead!
Warning: homebrew/php/php71: this formula has no --with-tidy option so it will be ignored!

==> Installing homebrew/php/php71 --with-gmp --with-httpd24 --with-debug --with-imap --with
==> Downloading https://php.net/get/php-7.1.8.tar.bz2/from/this/mirror
==> Downloading from https://secure.php.net/distributions/php-7.1.8.tar.bz2
######################################################################## 100.0%
==> ./configure --prefix=/usr/local/Cellar/php71/7.1.8_20 --localstatedir=/usr/local/var --sysconfdir
==> make
==> make install
==> Caveats

To enable PHP in Apache add the following to httpd.conf and restart Apache:
    LoadModule php7_module /usr/local/opt/php71/libexec/apache2/libphp7.so

    <FilesMatch .php$>
        SetHandler application/x-httpd-php
    </FilesMatch>

Finally, check DirectoryIndex includes index.php
    DirectoryIndex index.php index.html

The php.ini file can be found in:
    /usr/local/etc/php/7.1/php.ini

✩✩✩✩ Extensions ✩✩✩✩

If you are having issues with custom extension compiling, ensure that you are using the brew version, by placing /usr/local/bin before /usr/sbin in your PATH:

      PATH="/usr/local/bin:$PATH"

PHP71 Extensions will always be compiled against this PHP. Please install them using --without-homebrew-php to enable compiling against system PHP.

✩✩✩✩ PHP CLI ✩✩✩✩

If you wish to swap the PHP you use on the command line, you should add the following to ~/.bashrc, ~/.zshrc, ~/.profile or your shell's equivalent configuration file:
  export PATH="$(brew --prefix homebrew/php/php71)/bin:$PATH"

GMP has moved to its own formula, please install it by running: brew install php71-gmp

✩✩✩✩ FPM ✩✩✩✩

To launch php-fpm on startup:
    mkdir -p ~/Library/LaunchAgents
    cp /usr/local/opt/php71/homebrew.mxcl.php71.plist ~/Library/LaunchAgents/
    launchctl load -w ~/Library/LaunchAgents/homebrew.mxcl.php71.plist

The control script is located at /usr/local/opt/php71/sbin/php71-fpm

OS X 10.8 and newer come with php-fpm pre-installed, to ensure you are using the brew version you need to make sure /usr/local/sbin is before /usr/sbin in your PATH:

  PATH="/usr/local/sbin:$PATH"

You may also need to edit the plist to use the correct "UserName".

Please note that the plist was called 'homebrew-php.josegonzalez.php71.plist' in old versions of this formula.

With the release of macOS Sierra the Apache module is now not built by default. If you want to build it on your system you have to install php with the --with-httpd24 option. See  brew options php71 for more details.

To have launchd start homebrew/php/php71 now and restart at login:
  brew services start homebrew/php/php71
==> Summary
🍺  /usr/local/Cellar/php71/7.1.8_20: 347 files, 70.2MB, built in 5 minutes 5 seconds
```

安装完成后可以通过 `php -v`查看版本

### 修改 httpd.conf

`sudo vim /etc/apache2/httpd.conf`

按`/`搜索 `php5_module` 替换为日志输出中的 `LoadModule php7_module /usr/local/opt/php71/libexec/apache2/libphp7.so`  
并添加

```
<FilesMatch .php$>
    SetHandler application/x-httpd-php
</FilesMatch>
```

### php.ini

php.ini初始文件在 `/usr/local/etc/php/7.1/php.ini` 中

### 指定php-cli使用最新版本

添加到 `~/.bash_profile` 中

```
export PATH="$(brew --prefix homebrew/php/php71)/bin:$PATH"
```

**在终端里输入命令**，启动 Apache： `sudo apachectl start`  
- 关闭 Apache： `sudo apachectl stop`
- 重启 Apache：`sudo apachectl restart`
- 查看 Apache 版本：`httpd -v`

重启后在浏览器中输入`http://localhost`  或 `http://127.0.0.1` 出现 **It works!** 就表示运行正常..

### Errors

- 输入`sudo apachectl restart` 重启时报错

```
AH00557: httpd: apr_sockaddr_info_get() failed for xxx-Pro.local
AH00558: httpd: Could not reliably determine the server's fully qualified domain name, using 127.0.0.1. Set the 'ServerName' directive globally to suppress this message
httpd not running, trying to start
```

[`https://apple.stackexchange.com`](https://apple.stackexchange.com/questions/280099/apache-on-macos-sierra-ah00557-httpd-apr-sockaddr-info-get-failed-for-macbo)

修改`httpd.conf` 文件 中 `#ServerName www.example.com:80` 为 `ServerName www.your-web-server.com:80` ,如：`www.xinghe.php.com:80`

**特别注意** 当启动`httpd`的时候应该 
- 使用 `sudo /usr/sbin/apachectl restart` 
- 不要用 `sudo apachectl restart`

这是因为你安装了多个版本的Apache导致，一个是系统自带的，一个是你自己安装的


### 安装多个版本

[Mac OSX 多PHP版本共存](https://www.leocode.net/article/index/26.html)

## Root目录

Mac 中系统级的 Web 根目录：`/Library/WebServer/Documents`  



## Note

关于换行

> 尽管换行在 HTML 中的实际意义不是很大，但适当地使用换行可以使 HTML 代码易读且美观。PHP 会在输出时自动 **删除** 其结束符 `?>`后的一个换行。该功能主要是针对在一个页面中嵌入多段 PHP 代码或者包含了无实质性输出的 PHP 文件而设计，与此同时也造成了一些疑惑。如果需要在 PHP 结束符 `?>` 之后输出换行的话，可以在其后加一个**空格**，或者在最后的一个 `echo/print` 语句中加入一个换行 **<br/>**

## 参考文献

- [`w3school PHP教程`](http://www.w3school.com.cn/php/) 
- [`PHP中文手册`](http://php.net/manual/zh/) 
- [`awesome php`](https://github.com/ziadoz/awesome-php) `资源收集`
- [`PHP The Right Way`](https://github.com/codeguy/php-the-right-way/) `各种译本`

## 参考网站

- [PHP 中文网](http://www.php.cn/)

## 视频教程

- [PHP入门视频教程之一周学会PHP](http://www.php.cn/course/170.html)
