# microservice-config
spring:
  profiles:
    active:
      - dev

---
server: 
  port: 7003

spring:
  profiles: dev
  application:
    name: microservice-consumer-config-clent

eureka:
  client:
    register-with-eureka: false
    service-url: 
      defaultZone: http://eureka9001.com:9001/eureka

---
server: 
  port: 7004

spring:
  profiles: test
  application:
    name: microservice-consumer-config-clent

eureka:
  client:
    register-with-eureka: false
    service-url: 
      defaultZone: http://eureka9001.com:9001/eureka
