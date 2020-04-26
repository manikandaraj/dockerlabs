FROM centos:centos8
MAINTAINER Project Zeus <mani.jokasta@gmail.com>

RUN yum -y update
RUN yum -y install openssh-server passwd
RUN yum -y install epel-release
RUN yum clean all
RUN useradd mani
RUN echo mani:mani | chpasswd
RUN /usr/bin/ssh-keygen -A
EXPOSE 22
RUN rm -rf /run/nologin
CMD /usr/sbin/sshd -D
