FROM ubuntu:22.04

EXPOSE 8080

WORKDIR /usr/src/app

RUN apt-get update -y && apt-get install openjdk-8-jdk -y

COPY . .

RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
