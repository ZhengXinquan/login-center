# account

## 登录
## 依赖
dev: 127.0.0.1:8081/zz_js/index.js
pro: www.nanshanqiao.com/zz_js/index.js

## 其它
1. 由 `node-serve` 启动 为 `http://127.0.0.1:8082`
2. nginx 配置 转发到 `account.nanshanqiao.com`
```
	server {
        listen       80;
        server_name  account.nanshanqiao.com;
        location / {
            #root   C:\project\account;
            #index  index.html index.htm;
			proxy_pass  http://127.0.0.1:8082;
        }
    }
