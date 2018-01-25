FROM amazonlinux

RUN yum install openssh-server -y

RUN /usr/bin/ssh-keygen -A && \
    sed -ri 's/^#PermitRootLogin yes/PermitRootLogin yes/' /etc/ssh/sshd_config

ADD ./ssh/authorized_keys /root/.ssh/
RUN chmod 700 /root/.ssh
RUN chmod 600 /root/.ssh/*

CMD /usr/sbin/sshd -D
