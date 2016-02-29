FROM slintes/jre8

MAINTAINER Nils Petzall <nils.petzall@gmail.com>

RUN mkdir -p /opt/apache-ace-2.0.1-bin && \
  adduser -h /opt/apache-ace-2.0.1-bin -S -D -H ace
ADD http://apache.mirrors.spacedump.net/ace/apache-ace-2.0.1/apache-ace-2.0.1-bin.zip /tmp
RUN unzip /tmp/apache-ace-2.0.1-bin.zip  -d /opt/ && chown -R ace /opt/apache-ace-2.0.1-bin
EXPOSE 8080

USER ace
WORKDIR /opt/apache-ace-2.0.1-bin/server-allinone
CMD java -jar server-allinone.jar
