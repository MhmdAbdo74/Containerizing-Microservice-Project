FROM openjdk:8 AS BUILD_IMAGE
WORKDIR /usr/src/app/
#install maven
RUN apt update && apt install maven -y
#copy app file inside container 
COPY ./ /usr/src/app/
#build project 
RUN mvn install -DskipTests
FROM openjdk:8

WORKDIR /usr/src/app/
COPY --from=BUILD_IMAGE /usr/src/app/target/book-work-0.0.1-SNAPSHOT.jar ./book-work-0.0.1.jar

EXPOSE 9000
#run java artifact 
ENTRYPOINT ["java","-jar","book-work-0.0.1.jar"]
# Test
