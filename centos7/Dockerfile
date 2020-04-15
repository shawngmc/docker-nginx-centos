FROM centos:centos7
LABEL maintainer="Shawn McNaughton<shawngmc@gmail.com>"

RUN yum install -y wget openssl sed nginx &&\
    yum -y autoremove &&\
    yum clean all

COPY nginx.conf /etc/nginx/nginx.conf
COPY index.html /data/www/index.html
VOLUME [ "/data/www" ]
EXPOSE 80
USER nginx
CMD ["nginx", "-g", "daemon off;"]