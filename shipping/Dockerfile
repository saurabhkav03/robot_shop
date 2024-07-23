FROM debian AS build 
#Install maven and update
RUN apt update && apt-get install maven -y 
#Set working directory
WORKDIR /opt/shipping

COPY shipping/pom.xml /opt/shipping/
#Download all the dependencies as per the pom.xml file
RUN mvn dependency:resolve
# Copy the application source code
COPY shipping/src /opt/shipping/src
# Build the application
RUN mvn package

FROM openjdk:11-jre-slim

WORKDIR /opt/shipping

EXPOSE 8080

ENV CART_ENDPOINT=cart:8080
ENV DB_HOST=mysql

COPY --from=build /opt/shipping/target/shipping-1.0.jar shipping.jar

CMD ["java", "-jar", "shipping.jar"]
