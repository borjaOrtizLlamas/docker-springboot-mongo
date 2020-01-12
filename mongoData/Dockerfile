from mongo:4.2.1-bionic
EXPOSE 27017
ENV MONGO_INITDB_ROOT_USERNAME=borja
ENV MONGO_INITDB_ROOT_PASSWORD=borja
RUN groupadd -r borja && useradd -r -g borja borja
RUN DEBIAN_FRONTEND=nointeractive apt-get update -y --no-install-recommends && \
apt-get install -y --no-install-recommends locales && \
locale-gen en_US.UTF-8 && \
apt-get install -y --no-install-recommends software-properties-common vim  net-tools && \
apt-get clean -y 
