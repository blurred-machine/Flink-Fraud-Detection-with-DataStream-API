# Flink-Fraud-Detection-with-DataStream-API
This repo consists of a fraud detection system for alerting on suspicious credit card transactions. Using a simple set of rules, you will see how Flink allows us to implement advanced business logic and act in real-time.

To be able to run Flink, the only requirement is to have a working **Java 8 or 11** installation. 


## Run this project
### Create a maven project
```mvn
mvn archetype:generate \
    -DarchetypeGroupId=org.apache.flink \
    -DarchetypeArtifactId=flink-walkthrough-datastream-java \
    -DarchetypeVersion=1.11.2 \
    -DgroupId=frauddetection \
    -DartifactId=frauddetection \
    -Dversion=0.1 \
    -Dpackage=spendreport \
    -DinteractiveMode=false
```

### Import the java detector files and package the project
```mvn
mvn clean package
```
this will generate the .jar file, now use the jar file to run on the flink cluster. Take the jar file inside your flink repo and run the following commands.

1) start cluster:
```mvn
./bin/start-cluster.sh
```
2) run the jar on flink:
```mvn
./bin/flink run ./frauddetection-0.1.jar
```
3) Additionally, you can check Flink’s Web UI to monitor the status of the Cluster and running Job.
<br>Firstly, let's config the rest ports for the web UI
```yml
rest.port: 8081
rest.address: 0.0.0.0

```
Now we can access the UI at localhost port 8081 using the link [Flink Local UI](http://localhost:8081)
![UI](https://github.com/blurred-machine/Flink-Fraud-Detection-with-DataStream-API/blob/main/images/ui.png)
4) To stop the cluster:
```mvn
./bin/stop-cluster.sh
```




