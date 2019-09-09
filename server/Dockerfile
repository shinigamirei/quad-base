#Very similar to the springboot hello world Dockerfile

#try to use a multi stage file

FROM maven
WORKDIR /build
COPY pom.xml .
RUN mvn verify --fail-never
COPY . .
RUN mvn clean package

FROM openjdk:8
COPY target/Spring_Day_Two-0.0.1-SNAPSHOT.jar Server.jar
ENTRYPOINT ["java","-jar","Server.jar"]

