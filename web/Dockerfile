FROM zeeemughal/cent7-core:latest
COPY nginx.repo /etc/yum.repos.d/nginx.repo
RUN yum update -y
RUN yum install nginx
EXPOSE 22

#CMD [ "sh", "-c" , "service sshd restart && sh"]
CMD ["/usr/sbin/sshd","-D"]