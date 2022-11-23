## Configuration JMS
```
@Bean
    public MessageConverter jacksonJmsMessageConverter() {
        MappingJackson2MessageConverter converter = new MappingJackson2MessageConverter();
        converter.setTargetType(MessageType.TEXT);
        converter.setTypeIdPropertyName("_type");
        return converter;
    }

    @Bean
    public DefaultJmsListenerContainerFactory myFactory(SingleConnectionFactory connectionFactory,
                                                                  DefaultJmsListenerContainerFactoryConfigurer configurer) {
        DefaultJmsListenerContainerFactory factory = new DefaultJmsListenerContainerFactory();
        factory.setConnectionFactory(connectionFactory);
        configurer.configure(factory, connectionFactory);
        return factory;
    }
```

## Commande curl
```
curl -u admin:admin -XPOST -d "body={\"to\":\"info@example.com\",\"body\":\"Curl Topic Hello\"}" -d "_type=hepl.sysdist.activemq.topic.CustomMessage" -d "priority=high" http://localhost:8161/api/message/mytopic?type=topic
```