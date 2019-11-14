#### 起步

```cmd
# 安装 Node.js 环境
# 进入VueCli官网
https://cli.vuejs.org/zh/
# 安装VueCli 3.0
npm install -g @vue/cli
# OR
yarn global add @vue/cli
# 验证
vue --version # => 3.x.x
```

#### 创建一个项目

```cmd
vue create <project-name>
> pick a preset : Babel,Router,Vuex,CSS Pre-processors
> Use history mode for router
> Pick a CSS-processor (Less)
> In package.json
install.......
cd projectname
yarn serve

# 添加相关插件
yarn add axios moment reset-css
```

#### 清理默认生成的文件

#### 配置 vue.config.js

##### 配置axios 和 响应状态码

