# FROM tomcat:jre8-openjdk-slim-buster


# RUN apt-get update
# RUN apt-get install -y wget

 
# COPY ./payment-service/target/*.jar payment-service.jar

# EXPOSE 8080

# CMD ["java","-jar","payment-service.jar"]   

# Uses a supported, secure Eclipse Temurin OpenJDK 8 image
FROM eclipse-temurin:8-jre

# Install wget (repos work perfectly here)
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/*

COPY ./payment-service/target/*.jar payment-service.jar

EXPOSE 8080

CMD ["java", "-jar", "payment-service.jar"]
