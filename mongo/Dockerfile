# mongod process on latest CentOS

# See https://docs.docker.com/articles/dockerfile_best-practices/



# Base container on latest CentOS release
FROM centos

MAINTAINER Lei Ning <ninglei_1@sina.com>


# Copy yum repo config file to add MongoDB repo
COPY mongodb.repo /etc/yum.repos.d/
# Install mongod
RUN yum install -y mongodb-org-server

# Create default dbpath
RUN mkdir -p /data/db



# Execute the mongod binary on container startup
ENTRYPOINT [ "mongod" ]