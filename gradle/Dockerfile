FROM sbeliakou/centos:7.2
MAINTAINER Siarhei Beliakou

RUN yum install -y zip unzip wget which java-1.8.0-openjdk java-1.8.0-openjdk-devel && yum clean all

ENV SDKMAN_DIR="/usr/local/sdkman"

RUN curl -s https://get.sdkman.io | bash && \
    bash -c -i "sdk install gradle 3.2.1" && \
    bash -c -i "gradle --version"

ENV GRADLE_USER_HOME=/workspace
WORKDIR /workspace

ADD entrypoint.sh /usr/bin/entrypoint.sh

ENTRYPOINT ["/usr/bin/entrypoint.sh"]
CMD ["/bin/bash"]

