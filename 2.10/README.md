## Print.html
```
<!DOCTYPE html>
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8"/>
    <title>Spring MVC SYSDIST Demo </title>
</head>
<body>
<h1>Account List</h1>
<table>
    <tr>
        <th>ID</th>
        <th>Bank</th>
        <th>Amount</th>
    </tr>
    <tr th:each="account : ${accounts}">
        <td th:text="${account.getaccountId()}"></td>
        <td th:text="${account.getBank().getbankName()}"></td>
        <td th:text="${account.getaccountAmount()}"></td>
    </tr>
</table>
</body>
</html>
```

## MANIFEST-MF
```
Manifest-Version: 1.0
Main-Class: hepl.sysdist.springbootdemo.SpringbootdemoApplication
Class-Path: dom4j-2.1.3.jar jackson-databind-2.11.2.jar thymeleaf-spring
 5-3.0.11.RELEASE.jar spring-boot-starter-web-2.3.3.RELEASE.jar spring-b
 oot-autoconfigure-2.3.3.RELEASE.jar jackson-core-2.11.2.jar aspectjweav
 er-1.9.6.jar jandex-2.1.3.Final.jar jul-to-slf4j-1.7.30.jar jakarta.ann
 otation-api-1.3.5.jar snakeyaml-1.26.jar spring-boot-starter-jdbc-2.3.3
 .RELEASE.jar h2-1.4.200.jar LatencyUtils-2.0.3.jar log4j-to-slf4j-2.13.
 3.jar jackson-module-parameter-names-2.11.2.jar spring-aspects-5.2.8.RE
 LEASE.jar spring-boot-starter-validation-2.3.3.RELEASE.jar istack-commo
 ns-runtime-3.0.11.jar javassist-3.24.0-GA.jar spring-webmvc-5.2.8.RELEA
 SE.jar HikariCP-3.4.5.jar log4j-api-2.13.3.jar byte-buddy-1.10.14.jar s
 pring-jdbc-5.2.8.RELEASE.jar spring-boot-starter-logging-2.3.3.RELEASE.
 jar logback-classic-1.2.3.jar jakarta.transaction-api-1.3.3.jar jakarta
 .activation-api-1.2.2.jar spring-core-5.2.8.RELEASE.jar jakarta.xml.bin
 d-api-2.3.3.jar spring-boot-actuator-autoconfigure-2.3.3.RELEASE.jar hi
 bernate-core-5.4.20.Final.jar slf4j-api-1.7.30.jar jakarta.validation-a
 pi-2.0.2.jar micrometer-core-1.5.4.jar antlr-2.7.7.jar spring-orm-5.2.8
 .RELEASE.jar spring-boot-2.3.3.RELEASE.jar jakarta.persistence-api-2.2.
 3.jar spring-boot-starter-json-2.3.3.RELEASE.jar jackson-datatype-jsr31
 0-2.11.2.jar HdrHistogram-2.1.12.jar classmate-1.5.1.jar thymeleaf-extr
 as-java8time-3.0.4.RELEASE.jar spring-boot-actuator-2.3.3.RELEASE.jar j
 akarta.activation-1.2.2.jar spring-context-5.2.8.RELEASE.jar jakarta.el
 -3.0.3.jar jackson-annotations-2.11.2.jar spring-jcl-5.2.8.RELEASE.jar 
 spring-beans-5.2.8.RELEASE.jar spring-boot-starter-actuator-2.3.3.RELEA
 SE.jar jboss-logging-3.4.1.Final.jar spring-tx-5.2.8.RELEASE.jar spring
 -boot-starter-aop-2.3.3.RELEASE.jar tomcat-embed-websocket-9.0.37.jar s
 pring-boot-starter-data-jpa-2.3.3.RELEASE.jar spring-data-jpa-2.3.3.REL
 EASE.jar txw2-2.3.3.jar thymeleaf-3.0.11.RELEASE.jar hibernate-commons-
 annotations-5.1.0.Final.jar spring-data-commons-2.3.3.RELEASE.jar hiber
 nate-validator-6.1.5.Final.jar jackson-datatype-jdk8-2.11.2.jar tomcat-
 embed-core-9.0.37.jar logback-core-1.2.3.jar unbescape-1.1.6.RELEASE.ja
 r spring-expression-5.2.8.RELEASE.jar spring-boot-starter-thymeleaf-2.3
 .3.RELEASE.jar spring-web-5.2.8.RELEASE.jar spring-boot-starter-2.3.3.R
 ELEASE.jar jaxb-runtime-2.3.3.jar attoparser-2.0.5.RELEASE.jar spring-b
 oot-starter-tomcat-2.3.3.RELEASE.jar spring-aop-5.2.8.RELEASE.jar
```

## pom.xml
```
<dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-jpa</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-thymeleaf</artifactId>
        </dependency>
        <dependency>
            <groupId>com.h2database</groupId>
            <artifactId>h2</artifactId>
            <scope>runtime</scope>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <scope>test</scope>
            <exclusions>
                <exclusion>
                    <groupId>org.junit.vintage</groupId>
                    <artifactId>junit-vintage-engine</artifactId>
                </exclusion>
            </exclusions>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-validation</artifactId>
        </dependency>
    </dependencies>
    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
        </plugins>
    </build>
```