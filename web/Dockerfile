FROM centos:centos7
RUN yum update -y && yum install openssh-server -y
RUN sshd-keygen
RUN useradd -m zeeshan && echo "1234" | passwd zeeshan --stdin && mkdir /home/zeeshan/.ssh
COPY ../itos.pub /home/zeeshan/.ssh/authorized_keys
RUN chown -R zeeshan:zeeshan /home/zeeshan/.ssh && chmod 600 /home/zeeshan/.ssh/authorized_keys

 
EXPOSE 22

#CMD [ "sh", "-c" , "service sshd restart && sh"]
CMD ["/usr/sbin/sshd","-D"]