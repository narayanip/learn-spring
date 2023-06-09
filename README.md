Prerequisites
--
    Java Developoment Kit 11 higher
    
    Apache Maven 3.8.4 or higher

Database
--
    Modify pom.xml to use the required jdbc driver
    If using different database replace properties
    in project_home/src/main/resources/application.properties
```
##replace the property values if different database
    #the url for the database
    spring.datasource.url=jdbc:postgresql://localhost:5432/postgres
##the username for the database
    spring.datasource.username=jboss
##the password for the database
    spring.datasource.password=   
##the datasource.driver-class for the database
    spring.datasource.driver-class-name=org.postgresql.Driver           
##hibernate dialect
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQL82Dialect
```
Build Application
--
    From the project folder
        mvn clean install -DskipTests=true
        
Run Application Development Mode
---
    Make sure you have this dependency in pom.xml
```   
<dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-devtools</artifactId>
      <scope>runtime</scope>
      <optional>true</optional>
  </dependency>
 ```
  
    Start the applicaiton in dev mode
    This will allow hot reload of class

```
    mvn clean spring-boot:run
```    
Run Application
--
    Make sure the database server you have chosen is running
    From the project folder
        #this will run the server in port 8080 
        #if needed to run on a different port no. change 8080 to something else
        java -jar target/learn-spring.jar --server.port=8080
        
  


