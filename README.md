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

## Note

关于换行
```
尽管换行在 HTML 中的实际意义不是很大，但适当地使用换行可以使 HTML 代码易读且美观。PHP 会在输出时自动 **删除** 其结束符 ?> 后的一个换行。该功能主要是针对在一个页面中嵌入多段 PHP 代码或者包含了无实质性输出的 PHP 文件而设计，与此同时也造成了一些疑惑。如果需要在 PHP 结束符 ?> 之后输出换行的话，可以在其后加一个**空格**，或者在最后的一个 echo/print 语句中加入一个换行 **<br/>**
```

=====

## 参考文献

- [`w3school PHP教程`](http://www.w3school.com.cn/php/) 
- [`PHP中文手册`](http://php.net/manual/zh/) 
- [`awesome php`](https://github.com/ziadoz/awesome-php) `资源收集`
- [`PHP The Right Way`](https://github.com/codeguy/php-the-right-way/) `各种译本`
