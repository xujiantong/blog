1. pom配置

   ```
   1.create new project
   2.选择Maven -> Create from archetype -> 选择 maven-archetype-webapp
   3.GroupId: com.xxx  ArtifactId: xxx
   ```

2. 目录结构

   ```
   projectName
    -.idea [IDE配置]
    -src
    --main
    ---resources
    ---webapp
    ----WEB-INFO
    -----web.xml [web页面配置文件 上下文请求的监听 过滤器等]
    -pom.xml
   ```

   

