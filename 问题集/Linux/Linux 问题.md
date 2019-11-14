#### 常用命令

```cmd
pwd 获取文件

# 如何创建一个用户
# 如何给用户赋予权限
# 如何删除一个用户
userdel -r username

# cat 命令
```



#### Linux给用户添加 sudo权限

```
https://blog.csdn.net/sinat_36118270/article/details/62899093
```

```cmd
# 切换到root用户
su root
# /etc/sudoers 默认是只读的 对root来说也是,添加 可写 权限
chmod u+w /etc/sudoers
# 编辑sudoers文件
vi /etc/sudoers 
root ALL=(ALL) ALL
xujiantong ALL =(ALL) ALL
# youuser ALL=(ALL) ALL
# %youuser ALL=(ALL) ALL
# youuser ALL=(ALL) NOPASSWD: ALL
# %youuser ALL=(ALL) NOPASSWD: ALL

# 第一行:允许用户youuser执行sudo命令(需要输入密码).
# 第二行:允许用户组youuser里面的用户执行sudo命令(需要输入密码).
# 第三行:允许用户youuser执行sudo命令,并且在执行的时候不输入密码.
# 第四行:允许用户组youuser里面的用户执行sudo命令,并且在执行的时候不输入密码
#撤销sudoers文件写权限,命令:
chmod u-w /etc/sudoers
```

#### Linux系统下用户切换

```
su root
su xujiantong
```

