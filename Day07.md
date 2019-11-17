# Day07

----

### ZUUl

​		其实zuul和eureka给我的感觉是为了spring boot 过于spring boot了，这两个本质上是可以分割为两个中间件产品，但回过头讲，spring boot不就是微型中间件么~~

新建网关模块，引入

```xml
<dependency>  
    <groupId>org.springframework.cloud</groupId>  
    <artifactId>spring-cloud-starter-netflix-zuul</artifactId>
</dependency>
```

