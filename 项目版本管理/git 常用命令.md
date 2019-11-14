#### 将 git 仓库添加到非空目录

```cmd
# 1. 进入非空目录，假设是 /apps/blog
cd /apps/blog

# 2. git clone --no-checkout <git url> tmp 克隆仓库到tmp
git clone --no-checkout https://git.dev.tencent.com/loyeeb/vue-app.git tmp

# 3. 将 tmp 目录下的 .git 目录移到根目录
mv tmp/.git . 

# 4. 移除 tmp 文件夹
rmdir tmp

# 5.刷新
git reset --hard HEAD
```

