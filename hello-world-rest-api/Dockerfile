#Level1
#FROM openjdk:11
#EXPOSE 5020
#ADD target/hello-world-rest-api.jar hello-world-rest-api.jar
#ENTRYPOINT ["sh", "-c", "java -jar /hello-world-rest-api.jar"]

#Level2
FROM openjdk:11
ARG DEPENDENCY=target/dependency
COPY ${DEPENDENCY}/BOOT-INF/lib /app/lib
COPY ${DEPENDENCY}/META-INF /app/META-INF
COPY ${DEPENDENCY}/BOOT-INF/classes /app
ENTRYPOINT ["java","-cp","app:app/lib/*","com.example.rest.webservices.restfulwebservices.RestfulWebServicesApplication"]
