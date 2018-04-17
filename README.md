# KartacaStaj-101

$ mkdir KartacaStaj-101

$ cd KartacaStaj-101

clone everything

$ sudo docker build -t tomcat .

The result should be like this:

Sending build context to Docker daemon  67.07kB
Step 1/7 : FROM java
 ---> d23bdf5b1b1b
Step 2/7 : MAINTAINER Abdulkadir <abdulkadirazm@gmail.com>
 ---> Using cache
 ---> 605451848e21
Step 3/7 : RUN curl -O http://archive.apache.org/dist/tomcat/tomcat-7/v7.0.55/bin/apache-tomcat-7.0.55.tar.gz
 ---> Using cache
 ---> a7cf4201e560
Step 4/7 : RUN tar xzf apache-tomcat-7.0.55.tar.gz
 ---> Using cache
 ---> 23664e8fd687
Step 5/7 : ADD sample.war apache-tomcat-7.0.55/webapps/
 ---> Using cache
 ---> 0dd54d4a893b
Step 6/7 : CMD apache-tomcat-7.0.55/bin/startup.sh && tail -f apache-tomcat-7.0.55/logs/catalina.out
 ---> Using cache
 ---> 719fea0af12b
Step 7/7 : EXPOSE 8080
 ---> Using cache
 ---> abfb81008e49
Successfully built abfb81008e49
Successfully tagged tomcat:latest

$ sudo docker run -p 8080:8080 tomcat

Will be get the end of the result

INFO: Server startup in 625 ms

Finally

$ sudo docker-compose up

Hope everything will work successfully.
