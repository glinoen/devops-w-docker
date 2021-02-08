FROM openjdk:8

WORKDIR /app

RUN apt-get update && apt-get install git

RUN git clone https://github.com/docker-hy/spring-example-project.git app

RUN cd app && ./mvnw package

EXPOSE 8080

CMD [ "java", "-jar", "app/target/docker-example-1.1.3.jar" ]
