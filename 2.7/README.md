## Weld
```
<dependency>
	<groupId>org.jboss.weld</groupId>
	<artifactId>weld-api</artifactId>
	<version>2.3.Final</version>
</dependency>
```
```
<dependency>
	<groupId>org.jboss.weld.se</groupId>
	<artifactId>weld-se</artifactId>
	<version>2.4.8.Final</version>
	<scope>test</scope>
	<type>jar</type>
</dependency>
```

## Junit
```
<dependency>
	<groupId>junit</groupId>
	<artifactId>junit</artifactId>
	<version>4.13.1</version>
	<scope>test</scope>
</dependency>
```

## Hamcrest
```
<dependency>
	<groupId>org.hamcrest</groupId>
	<artifactId>java-hamcrest</artifactId>
	<version>2.0.0.0</version>
</dependency>
```

## CDI
```
<dependency>
	<groupId>javax.enterprise</groupId>
	<artifactId>cdi-api</artifactId>
	<version>2.0</version>
</dependency>
```

## Beans.xml
```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://xmlns.jcp.org/xml/ns/javaee"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/javaee http://xmlns.jcp.org/xml/ns/javaee/beans_1_1.xsd"
	 bean-discovery-mode = "all">
</beans>
```