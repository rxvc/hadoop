FROM rxvc/openjdk:8-jdk-alpine
MAINTAINER Rodrigo Vallejo <rxvallejoc@gmail.com>

ENV HADOOP_VERSION 2.7.7
ENV HADOOP_URL http://apache.cs.utah.edu/hadoop/common/hadoop-$HADOOP_VERSION/hadoop-$HADOOP_VERSION.tar.gz

RUN set -x \
	&& apk add --no-cache curl bash perl \
	&& curl -fSL "$HADOOP_URL" -o /tmp/hadoop.tar.gz \
	&& tar -xvf /tmp/hadoop.tar.gz  \
	&& mkdir -p /opt/ \
	&& mv /hadoop-$HADOOP_VERSION /opt/ \
	&& rm /tmp/hadoop.tar.gz*
    
RUN ln -s /opt/hadoop-$HADOOP_VERSION/etc/hadoop /etc/hadoop
RUN cp /etc/hadoop/mapred-site.xml.template /etc/hadoop/mapred-site.xml
RUN mkdir /opt/hadoop-$HADOOP_VERSION/logs

RUN mkdir /hadoop-data

ENV HADOOP_PREFIX=/opt/hadoop-$HADOOP_VERSION
ENV HADOOP_CONF_DIR=/etc/hadoop
ENV MULTIHOMED_NETWORK=1

ENV USER=root
ENV PATH $HADOOP_PREFIX/bin/:$PATH

ADD entrypoint.sh /entrypoint.sh
RUN chmod a+x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
