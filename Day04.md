# Day04

-----

Spring Boot 工程创建

直接在<https://start.spring.io/> 创建即可，选中选定的maven



添加actuator


```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```


添加，开启对全部endpoint的扫描


```
management.endpoints.web.exposure.include=*
```


<https://docs.spring.io/spring-boot/docs/2.0.6.RELEASE/reference/htmlsingle/#production-ready-endpoints-exposing-endpoints> endpoint对应解释参照



添加 swagger

```
<dependency>
    <groupId>io.springfox</groupId>
    <artifactId>springfox-swagger2</artifactId>
    <version>2.9.0</version>
</dependency>
<dependency>
    <groupId>io.springfox</groupId>
    <artifactId>springfox-swagger-ui</artifactId>
    <version>2.9.0</version>
</dependency>
```

swagger配置参见代码

