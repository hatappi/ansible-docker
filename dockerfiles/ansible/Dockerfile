FROM ansible/centos7-ansible

RUN yum install openssh-clients -y

ADD ./ssh/id_rsa /root/.ssh/ 
RUN chmod 700 /root/.ssh
RUN chmod 600 /root/.ssh/*

