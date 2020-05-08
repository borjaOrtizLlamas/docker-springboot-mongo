FROM amd64/openjdk:8u232-jdk
EXPOSE 8080
RUN DEBIAN_FRONTEND=nointeractive apt-get update -y --no-install-recommends && \
apt-get install -y --no-install-recommends locales && \
locale-gen en_US.UTF-8 && \ 
apt-get install -y --no-install-recommends software-properties-common git maven
RUN git clone https://github.com/borjaOrtizLlamas/springboot.git /tmp/springboot && \
cd /tmp/springboot && mkdir /logs && mvn clean install
CMD ["java","-jgs-rest-service-0.1.0.jar", "com.borja.Aplication"] 
#ONBUILD SIRVEar","/tmp/springboot/target/ PARA HACER COSAS SI NO SOMOS LA IMAGEN BASE