##1. UC通信息不成功##

相关文件：config/config_ucenter.php, uc_server/data/config.inc.php

表：pre_ucenter_applications

说明：新 Discuz X3.4 集成了 uc-center, 所以配置路径不需要加/uc_center。 在页面可以抓到访问的地址是 https://bbs.example.com/api/./uc.php

处理方法：
	1. uc_server/data/config.inc.php 中增加编码配置 define('CHARSET', 'utf-8'); 
	2. ucenter -> UCenter 设置 -> 检查 uc key 是否合法(与config_ucenter.php是否相同)， 确认后提交即可。

参考：https://jingyan.baidu.com/article/48b37f8d4745c21a646488a0.html


##2. 复制短连接问题##

文件：/template/default/forum/viewthread.htm

处理方法： 查找，lang share_url_copy , 删除此行中$fromuid。

参考：[http://www.discuz.net/thread-3642983-1-1.html](http://www.discuz.net/thread-3642983-1-1.html)


##3. 无上传按钮##

原因：chrome不支持跨站点小swf文件访问

处理办法：static/js/upload.js static/js/swfupload.js 文件,  swf地址改为 "/static/image/common/swfupload.swf" 不使用 CDN 地址, 直接走论坛站点。


##4. 乱码问题##

1. uc_server/data/config.inc.php 中增加编码配置 define('CHARSET', 'utf-8'); 

2. default/forum/discuz.htm newsetuser 显示乱码，暂时屏蔽了。后面找时间看。

##5. Logo及图片问题##

这个很好解决，给一个正确的地址和图片即可。

favicon.ico: 一定保证论坛文件正确，这个文件，不走 CDN

其他图片： 大多数是使用 CDN 的， 需要保证 CDN 上图片正确。
