# Sample Sidecar application 

Run the application in the standard way of running a springboot application 

```
mvn clean package
java -jar tar target/ sample-sidecar-0.0.1-SNAPSHOT.jar --spring.profiles.active=dev --spring.cloud.config.label=dev --sidecar.port=5000
```
