<h1 align="center">git仓库迁移</h1>

# checkout所有分支到本地
```
git clone xxx
git branch -r | grep -v '\->' | while read remote; do git branch --track "${remote#origin/}" "$remote"; done
git fetch --all
git pull --all
```

# 推送到远程
```
git push --mirror http://xxxx
```