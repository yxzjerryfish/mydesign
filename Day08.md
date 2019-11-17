# Day08

-----

微服务调用：

1. 直接调用：

2. Ribbon调用

3. Feign调用

## 直接调用：

需增加一个resttemplate注解

```java
@Bean
RestTemplate restTemplate(){    return new RestTemplate();}
```

然后自动装配：

```java
@Autowired
RestTemplate restTemplate;
```

这样，在服务调用方就可以通过：

```java
public String sayHello(){      
    return restTemplate.getForObject("http://localhost:9090/hello",String.class);
}
```

其中localhost 是微服务地址，来访问微服务。



***

## Ribbon调用

ribbon调用只需要在resttemplate上面增加一个@LoadBalanced注解，然后就可以如下调用：

```java
@ApiOperation(value = "没有用feign来尝试调用微服务")
@RequestMapping("/nofeign/hello")
public String getnofeignHello(){    
    ResponseEntity<String> responseEntity = restTemplate.getForEntity("http://DATABASE/hello",String.class);    
    return responseEntity.getBody();
}
```

其中DATABASE是暴露在Eureka的服务名



## Feign调用

feign调用会在下一部分弄完