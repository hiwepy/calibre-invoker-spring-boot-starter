# calibre-invoker-spring-boot-starter
Spring Boot Starter For Calibre Invoker

### 说明

 > 基于 maven-invoker 的 Spring Boot Starter 实现

1. 整合 maven-invoker

### Maven

``` xml
<dependency>
	<groupId>${project.groupId}</groupId>
	<artifactId>calibre-invoker-spring-boot-starter</artifactId>
	<version>${project.version}</version>
</dependency>
```

### Sample

```java

import javax.annotation.PostConstruct;

import org.apache.maven.spring.boot.ext.CalibreInvokerTemplate;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class Application {
	
	@Autowired
	private CalibreInvokerTemplate calibreInvokerTemplate;
	
	@PostConstruct
	private void init() {
		
		//calibreInvokerTemplate.deploy(file, groupId, artifactId, version, packaging, url, repositoryId);
		//calibreInvokerTemplate.deploy(basedir, file, groupId, artifactId, version, packaging, url, repositoryId);
		
		//calibreInvokerTemplate.execute(basedir, goals);
		//calibreInvokerTemplate.execute(basedir, goals);
		
	}
	
	public static void main(String[] args) throws Exception {
		SpringApplication.run(Application.class, args);
	}

}

```
