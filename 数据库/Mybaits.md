##### mybatis generator详解

```
http://mybatis.org/generator/configreference/table.html
```

##### mybatis 日志详解

```
https://blog.csdn.net/fageweiketang/article/details/80767532
```



#### mybatis 如何返回新增数据的id

##### Method 1

```xml
<insert id="insertAndGetId" useGeneratedKeys="true" keyProperty="userId" parameterType="com.chenzhou.mybatis.User">
    insert into user(userName,password,comment)
    values(#{userName},#{password},#{comment})
</insert>
```

```
useGeneratedKeys="true" 表示给主键设置自增长
keyProperty="userId"  表示将自增长后的Id赋值给实体类中的userId字段。
parameterType="com.chenzhou.mybatis.User" 这个属性指向传递的参数实体类
这里提醒下，<insert></insert> 中没有resultType属性，不要乱加。
实体类中uerId 要有getter() and setter(); 方法
```

##### Method2

```xml
<!-- 插入一个商品 -->
<insert id="insertProduct" parameterType="domain.model.ProductBean" >
       <selectKey resultType="java.lang.Long" order="AFTER" keyProperty="productId">
          SELECT LAST_INSERT_ID()
      </selectKey>
        INSERT INTO t_product(productName,productDesrcible,merchantId)values(#{productName},#{productDesrcible},#{merchantId});
</insert>
```

```
<insert></insert> 中没有resultType属性，但是<selectKey></selectKey> 标签是有的。

order="AFTER" 表示先执行插入语句，之后再执行查询语句。

可被设置为 BEFORE 或 AFTER。

如果设置为 BEFORE,那么它会首先选择主键,设置 keyProperty 然后执行插入语句。

如果设置为 AFTER,那么先执行插入语句,然后是 selectKey 元素-这和如 Oracle 数据库相似,可以在插入语句中嵌入序列调用
keyProperty="userId"  表示将自增长后的Id赋值给实体类中的userId字段。

SELECT LAST_INSERT_ID() 表示MySQL语法中查询出刚刚插入的记录自增长Id.

实体类中uerId 要有getter() and setter(); 方法
```

```java
调用
　UserAccount userAccount1  = new UserAccount();
        userAccount1.setAccountname("test2");
        userAccount1.setPassword("test2");
        userAccount1.setRegistos("IOS");
        userAccount1.setStutas(0);
        userAccount1.setCreatetime(System.currentTimeMillis());
        userAccount1.setImei("test");
        userAccount1.setChannel("test");
        userAccount1.setRegistip("0.0.0.0");
        int i = userAccountMapper.insertSelective(userAccount1);
        System.out.println(userAccount1.getAccountid());
```

