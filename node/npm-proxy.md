<h1 align="center">npm设置代理</h1>

# 查看npm配置
```
npm config list
```

# 设置代理

```
npm config set proxy=http://127.0.0.1:8087
```

# https
```
npm config set https-proxy http://server:port
```

# 代理用户名和密码
```
npm config set proxy http://username:password@server:port
npm confit set https-proxy http://username:password@server:port
```

# 取消代理
```
npm config delete proxy
npm config delete https-proxy
```