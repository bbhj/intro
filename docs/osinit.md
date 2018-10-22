##宝贝回家主机初始化##

###1. 安装 Nginx###

	`sudo yum install pcre-devel zlib-devel
	`./configure --prefix=/data/app/nginx --with-compat --add-dynamic-module=nginx-ipip-module 
	`make && make install

###日志清理###

	/etc/logrotate.d/nginx

/data/app/nginx/logs/error.log {
    su work work
    create 0644 work work
    daily
    rotate 10
    missingok
    notifempty
    compress
    sharedscripts
    postrotate
        /bin/kill -USR1 `cat /data/app/nginx/run/nginx.pid 2>/dev/null` 2>/dev/null || true
    endscript
}

###3. PHP7 安装###

###4. 设置安全组策略###

	1. 默认安全组放通全部端口

	2. ssh http https icmp

	3. default
