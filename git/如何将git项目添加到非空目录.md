#### 如何将git项目添加到非空目录?

```makefile
1. 进入非空目录，假设是 /apps/blog

2. git clone --no-checkout https://git.xxx.net/xxx/xxx.git tmp
eg.git clone --no-checkout https://git.dev.tencent.com/loyeeb/vue-app.git tmp

3. mv tmp/.git .   #将 tmp 目录下的 .git 目录移到当前目录

4. rmdir tmp

5. git reset --hard HEAD
```



