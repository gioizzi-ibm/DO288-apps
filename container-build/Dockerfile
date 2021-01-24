# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

LABEL io.openshift.expose-service="8080:http" /
	io.k8s.description="A basic HTTP Server app for DO288 course" /
        io.k8s.display-name="Apache HTTP Server" /
        io.openshift.tags="apache, httpd"

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf
RUN chgrp -R 0 /var/log/httpd /var/run/httpd && /
    chmod -R g=u /var/log/httpd /var/run/httpd

USER 1001

EXPOSE 8080
