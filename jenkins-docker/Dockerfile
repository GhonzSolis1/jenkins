FROM centos 

LABEL version=1.0 
LABEL description="Esto es una imagen apache"
LABEL vendor=Gonzalo

RUN yum install httpd -y

COPY beryllium /var/www/html

RUN echo "$(whoami)" > /var/www/html/user1.html

RUN useradd ghonz

USER ghonz

RUN echo "$(whoami)" > /tmp/user2.html

USER root

RUN cp /tmp/user2.html /var/www/html/user2.html

CMD apachectl -DFOREGROUND