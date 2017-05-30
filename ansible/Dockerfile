FROM sbeliakou/centos

RUN yum update -y && \
    yum install -y python-pip python-devel && \
    yum install -y gcc openssl-devel && \
    yum clean all

RUN pip install -U pip setuptools && \
    pip install ansible==2.2.1 requests termcolor

CMD ansible --version
