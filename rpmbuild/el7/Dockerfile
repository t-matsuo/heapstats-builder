FROM centos:7
LABEL maintainer "Yasumasa Suenaga <yasuenag@gmail.com>"

RUN yum upgrade -y \
  && yum install -y gcc-c++ java-1.8.0-openjdk-devel \
                    ant binutils-devel tbb-devel autoconf automake rpm-build \
                    wget net-snmp-devel pcre-devel make which
RUN wget http://repos.fedorapeople.org/repos/dchen/apache-maven/epel-apache-maven.repo -O /etc/yum.repos.d/epel-apache-maven.repo
RUN yum install -y apache-maven

ADD build.sh .

ENTRYPOINT ["./build.sh"]

