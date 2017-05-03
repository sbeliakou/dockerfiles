FROM scratch

MAINTAINER Siarhei Beliakou (sbeliakou@gmail.com)
ADD   centos.tar.gz /

RUN   yum install -y epel-release && \
      yum update -y && \
      yum clean all

LABEL architecture="amd64" \
      OS="CentOS" \
      License=GPLv2 \
      maintainer="Siarhei Beliakou (sbeliakou@gmail.com)"

# Default command 
CMD ["/bin/bash"]

