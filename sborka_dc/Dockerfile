FROM ubuntu:18.04

RUN apt-get update
RUN apt-get install -y default-jdk git maven

RUN mkdir -p /home/ubuntu/build
RUN mkdir -p /app
WORKDIR /home/ubuntu/build/
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
WORKDIR /home/ubuntu/build/boxfuse-sample-java-war-hello/
RUN mvn package

RUN cp /home/ubuntu/build/boxfuse-sample-java-war-hello/target/hello-1.0.war /app/hello.war

#EXPOSE 80
#CMD ["nginx", "-g", "daemon off;"]
