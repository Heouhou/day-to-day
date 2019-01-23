### Spring-boot 
1.
  
  ```java
  //该注解来标注一个主程序类,这说明是一个Spring Boot 应用
  @SpringBootApplication
public class SpringBoot01HelloQuickApplication {

    public static void main(String[] args) {
        //用来启动springboot
        SpringApplication.run(SpringBoot01HelloQuickApplication.class, args);
    }
}
  ```
  
  2
  
  ```xml
  <!-- 这个插件,可以将应用程序打包成一个执行Jar包 -->
  <build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
        </plugin>
    </plugins>
</build>
  ``` 
  
  
  pom
  
  
  
  
  ```xml
      <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>1.5.20.BUILD-SNAPSHOT</version>
        <relativePath/> <!-- lookup parent from repository -->
    </parent>
    
    他的父项目是
    
    
    <parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-dependencies</artifactId>
		<version>1.5.20.BUILD-SNAPSHOT</version>
		<relativePath>../../spring-boot-dependencies</relativePath>
	</parent>
    他来真正管理spring boot 应用里面所有依赖版本
  ```
  
  
  


springboot版本仲裁中心
以后我们导入依赖默认是不需要版本号的  但dependencies里面没有的还是需要




注解


@ResponseBody

这个类的所有方法返回的数据直接返回给浏览器,如果是对象还自动转换为Json数据



@PropertySource("classpath:datasource.properties")

作用：加载指定的properties配置文件




@Component //  将下面的组件加到容器中
@ConfigurationProperties(prefix = "person")//只有这个组件是容器中的组件，才能提供到容器中
@Validated


@ImportResource
作用：导入Spring配置文件，并且让这个配置文件生效


