FROM amd64/openjdk:8u232-jdk
EXPOSE 8080
COPY /ssh /root/.ssh
COPY maven-3.6.3/ /etc/maven
ENV MAVEN_HOME /etc/maven
ENV PATH="/etc/maven/bin:${PATH}"
RUN DEBIAN_FRONTEND=nointeractive apt-get update -y --no-install-recommends && \
apt-get install -y --no-install-recommends locales && \
locale-gen en_US.UTF-8 && \ 
apt-get install -y --no-install-recommends software-properties-common git && \ 
chmod 700 /root/.ssh/id_rsa
RUN git clone https://github.com/borjaOrtizLlamas/springboot.git /tmp/springboot && \
cd /tmp/springboot && mkdir /logs && mvn clean install
CMD ["java","-jar","/tmp/springboot/target/gs-rest-service-0.1.0.jar", "com.borja.Aplication"] 

#ONBUILD SIRVE PARA HACER COSAS SI NO SOMOS LA IMAGEN BASE