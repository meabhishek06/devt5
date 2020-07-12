FROM centos

RUN yum install wget tar -y
RUN wget https://github.com/prometheus/prometheus/releases/download/v2.19.2/prometheus-2.19.2.linux-amd64.tar.gz
RUN mkdir /promdata
RUN tar -xzf prometheus-2.19.2.linux-amd64.tar.gz
RUN cp -rf  prometheus-2.19.2.linux-amd64/* /promdata	
RUN cp /promdata/prometheus /usr/bin


CMD prometheus --config.file=/promdata/prometheus.yml