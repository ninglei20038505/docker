# Dockerizing MongoDB: Dockerfile for building MongoDB images
FROM nitra/centos7
MAINTAINER Nitra  
#Install MONGO3
ADD mongodb.repo /etc/yum.repos.d/mongodb.repo
RUN yum install -y mongodb-org numactl
#Install locale
RUN rm -rf /etc/localtime
RUN ln -s /usr/share/zoneinfo/Europe/Kiev /etc/localtime
RUN sed -i "s/4096/32000/"  /etc/security/limits.d/20-nproc.conf
# Expose port #27017 from the container to the host
EXPOSE 27017