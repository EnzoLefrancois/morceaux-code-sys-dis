## print.html
```
<!DOCTYPE html>
<html lang="en" xmlns:th="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="UTF-8">
    <title>Cool Message</title>
</head>
<body>
<p th:text="'Message  : ' + ${message}" />
</body>
</html>
```

## beans.xml
```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">
    <bean id="questiongenerator" class="hepl.sysdist.beanxml.model.MessageGenerator">
        <constructor-arg >
            <list>
                <value>Pourquoi ?</value>
                <value>Qui ?</value>
                <value>Comment ?</value>
            </list>
        </constructor-arg>
    </bean>
</beans>
```