FROM zeeemughal/cent7-core:latest
COPY nginx.repo /etc/yum.repos.d/nginx.repo
RUN yum update -y
RUN yum install nginx -y
RUN yum install net-tools -y
COPY newdefault.conf /etc/nginx/conf.d/default.conf
EXPOSE 22

#CMD [ "sh", "-c" , "service sshd restart && sh"]
CMD ["nginx", "-g", "daemon off;"]