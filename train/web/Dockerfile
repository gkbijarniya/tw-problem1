FROM fabric8/java-alpine-openjdk8-jdk:1.2

# Set environment

EXPOSE 8080

#Add the web app and jetty runner
WORKDIR /web/
ADD http://central.maven.org/maven2/org/mortbay/jetty/jetty-runner/7.6.5.v20120716/jetty-runner-7.6.5.v20120716.jar ./jetty-runner.jar    
ADD https://s3.amazonaws.com/infra-assessment/companyNews.war  ./

CMD java -jar jetty-runner.jar companyNews.war

