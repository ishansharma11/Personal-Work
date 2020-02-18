					Instructions to run "Kafka" on your workstation.

Please follow the below step by step instructions:

Step 1:
i)Download and Setup Java 8 JDK.
ii)Download the Kafka binaries from https://kafka.apache.org/downloads (Under version 2.0.0 download Scala 2.12  - kafka_2.12-2.0.0.tgz (asc, sha512) ).

Step 2: Extract in C drive

Step 3:Set Path: 
i.e goto kafka_2.12-2.0.0-->bin-->windows and copy its path,
then goto environmentvariables-->Path-->Edit-->New-->(Paste  C:\kafka_2.12-2.0.0\bin\windows)

Step 4: Create a new folder named "data" inside "kafka_2.12-2.0.0" folder. Add two new folders named "zookeeper" and "kafka" inside "data" folder.

Step 5: Copy the path of zookeeper folder i.e (C:\kafka_2.12-2.0.0\data\zookeeper)

Step 6: Goto kafka_2.12-2.0.0-->config-->zookeeper.properties then goto line 16 and replace /tmp/zookeeper by  C:/kafka_2.12-2.0.0/data/zookeeper. (i.e zookeeper path but with SLASHES REVERSED)

Step 7: Now in cmd navigate to "kafka_2.12-2.0.0" folder ( i.e cd C:\kafka_2.12-2.0.0 ) and 
Start Zookeeper in one command line by typing the following command:
zookeeper-server-start.bat config\zookeeper.properties   ,
Your zookeeper will start running.  (Note: If the above command doesn't work then open your cmd as administrator and do the same )

Step 8: Copy the path of kafka folder i.e (C:\kafka_2.12-2.0.0\data\kafka)

Step 9: Goto kafka_2.12-2.0.0-->config-->server.properties then goto line 60 and replace /tmp/kafka-logs by  C:/kafka_2.12-2.0.0/data/kafka. (i.e kafka folder path but with SLASHES REVERSED)

Step 10: Now open another cmd and navigate to "kafka_2.12-2.0.0" folder ( i.e cd C:\kafka_2.12-2.0.0 ) and Start kafka-server in that command line by typing the following command:
kafka-server-start.bat config\server.properties.
Your kafka will start running. (Note: If the above command doesn't work then open your cmd as administrator and do the same )

Step 11: Keep zookeeper and kafka-server running in the background and run your ProducerDemoKeys.java in IntelliJ and then run ConsumerDemo.java in IntelliJ.




