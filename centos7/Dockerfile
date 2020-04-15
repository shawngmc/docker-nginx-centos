FROM centos:centos7
LABEL maintainer="Shawn McNaughton<shawngmc@gmail.com>"

COPY nginx.repo /etc/yum.repos.d/nginx.repo

RUN yum update -y &&\
    yum install -y wget openssl sed nginx &&\
    yum -y autoremove &&\
    yum clean all 

COPY nginx.conf /etc/nginx/nginx.conf
COPY index.html /data/www/index.html
VOLUME [ "/data/www" ]
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
