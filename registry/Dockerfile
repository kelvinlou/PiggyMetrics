FROM goodrainapps/maven:jdk8-alpine
MAINTAINER guox <guox@goodrain.com>

# package
COPY . /app
WORKDIR /app
RUN mvn -s maven-settings.xml -B -DskipTests=true -Dmaven.repo.local=/tmp/cache clean install

CMD ["java", "-Xmx200m", "-jar", "/app/target/registry.jar"]

EXPOSE 8761
