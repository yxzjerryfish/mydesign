# Day06

----

Eureka

引入maven

```
<properties>
    <spring-cloud.version>Greenwich.SR1</spring-cloud.version>
</properties>
```

```    &lt;dependencyManagement&gt;
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
</dependency>
```

```
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-dependencies</artifactId>
            <version>${spring-cloud.version}</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

spring boot注解添加
>@EnableEurekaServer

