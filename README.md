# Flink-Fraud-Detection-with-DataStream-API
Credit card fraud is a growing concern in the digital age. Criminals steal credit card numbers by running scams or hacking into insecure systems. Stolen numbers are tested by making one or more small purchases, often for a dollar or less. If that works, they then make more significant purchases to get items they can sell or keep for themselves.

In this tutorial, you will build a fraud detection system for alerting on suspicious credit card transactions. Using a simple set of rules, you will see how Flink allows us to implement advanced business logic and act in real-time.


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
this will generate the .jar file, now use the jar file to run on the flink cluster.
1) start cluster
```mvn
./bin/start-cluster.sh
```
2) run the jar
```mvn
run ./Detector.jar
```
3) Additionally, you can check Flink’s Web UI to monitor the status of the Cluster and running Job.
[Flink Local UI](http://localhost:8080)




