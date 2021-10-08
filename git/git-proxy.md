<h1 align="center">git设置代理</h1>

# 设置代理
```
git config --global http.proxy http://127.0.0.1:1080
git config --global https.proxy https://127.0.0.1:1080
```

# 删除代理
```
git config --global --unset http.proxy
git config --global --unset https.proxy
```
