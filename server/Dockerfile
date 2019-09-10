#Very similar to the springboot hello world Dockerfile

#try to use a multi stage file

FROM maven as maven
WORKDIR /build
COPY . .
RUN mvn clean package

FROM java:8
WORKDIR /server
COPY --from=maven /build/target/Spring_Day_Two-0.0.1-SNAPSHOT.jar Server.jar
ENTRYPOINT ["java","-jar","Server.jar"]

