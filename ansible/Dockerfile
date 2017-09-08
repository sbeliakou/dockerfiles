FROM sbeliakou/centos

RUN yum update -y && \
    yum install -y python-pip python-devel && \
    yum install -y gcc openssl-devel rsync make file autoconf automake libtool && \
    yum clean all

RUN pip install -U pip setuptools && \
    pip install requests termcolor jmespath jq

RUN pip install ansible==2.3.2 ansible-modules-hashivault

ADD ansible.cfg /etc/ansible/ansible.cfg

ENV ANSIBLE_LOCAL_TEMP=/tmp
ENV ANSIBLE_FORCE_COLOR=true
ENV PYTHONUNBUFFERED=1

CMD ansible --version
