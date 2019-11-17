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

将其注册到eureka上

```yaml
eureka:  
	client:    
		serviceUrl:      
			defaultZone: http://localhost:1111/eureka
```

配置映射

```yaml
zuul:  
	routes:    
		route-name:      
			service-id: DATABASE      
			path: /database
```

在这个版本中，因为只是一个简单的demo，只做到这些，等后续再来实现其余功能

