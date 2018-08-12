##论坛##

[BBS](https://bbs.baobeihuijia.com) 主要由腾讯志愿者进行维护。 早期论坛采用 Discuz + CDB 搭建, 编码 GBK。

于2018年8月12日，已升级至 Discuz X3.4 UTF8 版本。

##项目地址##

Github: [https://github.com/bbhj/bbs.baobeihuijia.com](https://github.com/bbhj/bbs.baobeihuijia.com)

BBS 项目进度及需求后续会使用 Trello 来来进行管理。Trello 地址：[trello.com/b/Yyb1ovjP/bbhj](trello.com/b/Yyb1ovjP/bbhj)

##已处理问题##

1. 腾讯云 CVM 主机从基础网迁移至 VPC网络。(目标是支持 docker 部署)

2. 图片无法上传问题，已修复。

3. 腾讯云 CDB 已从 mysql 5.5 GBK 升级到 mysql 5.7 UTF8MB4。

4. Discuz X3.4 当前是从官方开源拉取的。 Discuz地址：[https://gitee.com/ComsenzDiscuz/DiscuzX](https://gitee.com/ComsenzDiscuz/DiscuzX)

以上操作均有备份，如有需要请与 Dean 联系。

##ChangLog##

1. default/forum/discuz.htm newsetuser 显示乱码，暂时屏蔽了。后面找时间看。

2. static/js/upload.js static/js/swfupload.js 文件提供由于chrome不支持跨站点访问，所以改为 "/static/image/common/swfupload.swf" 不使用 CDN 地址。

3. 首页的滚动图片正规的版本里没有， 需要重新处理一下。

##后续跟进##

1. 用户注册，UC 通信息问题。

2. static cdn 中包含以前的 GBK 文件，需要重新删除，上传一份 UTF8 的文件。

3. static cdn 中 uc_server 的图片也应该需要上传一份的。  请使用coscmd 上传。

4. attachment 域名的处理逻辑，需要再确认一下。

5. 看一下 avatar 能不能和 uc_server 的 avatar 合并在同一个域名里

##人员需求##

希望有 1名前端 + 2名php 开发跟进行项目，每周例行对论坛进行维护。
