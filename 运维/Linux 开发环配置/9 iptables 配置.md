#### 防火墙常用命令

```cmd
#vm虚拟机启动tomcat，本机访问不到问题
#iptables 未设置 解决方案https://blog.csdn.net/LTsunny/article/details/79417443
# 启动
service iptables start 
# 停止
service iptables stop  
# 重启防火墙命令
sudo service iptables restart
```

#### 常用编辑

```cmd
sudo vim /etc/sysconfig/iptables
#########
-A INPUT -p TCP --dport 61001:62000 -j ACCEPT
-A OUTPUT -p TCP --sport 61001:62000 -j ACCEPT
-A INPUT -p TCP --dport 20 -j ACCEPT
-A OUTPUT -p TCP --sport 20 -j ACCEPT
-A INPUT -p TCP --dport 21 -j ACCEPT
-A OUTPUT -p TCP --sport 21 -j ACCEPT
-A INPUT -p tcp -m state --state NEW -m tcp --dport 80 -j ACCEPT
########
#:wq 保存退出
# 重启防火墙命令
sudo service iptables restart
```

