# Maven配置

### 一、Docker镜像服务器配置

```xml
    <server>
        <id>docker-registry</id>
        <username>admin</username>
        <password>123456</password>
        <configuration>
            <email>admin@example.com</email>
        </configuration>
    </server>
```

### 二、Maven镜像服务器配置

```xml
    <mirror>
      <id>alimaven</id>
      <mirrorOf>central</mirrorOf>
      <name>aliyun maven</name>
      <url>http://maven.aliyun.com/nexus/content/groups/public/</url>
    </mirror>
```

### 三、默认JDK配置

```xml
  	<profile>
	    <id>jdk18</id>
	    <activation>
	        <activeByDefault>true</activeByDefault>
	        <jdk>1.8</jdk>
	    </activation>
	    <properties>
	        <maven.compiler.source>1.8</maven.compiler.source>
	        <maven.compiler.target>1.8</maven.compiler.target>
	        <maven.compiler.compilerVersion>1.8</maven.compiler.compilerVersion>
	    </properties>
	</profile>
```

