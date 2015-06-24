FROM centos:7

ENV CONSUL_VERSION 0.5.2

RUN curl -fLO https://dl.bintray.com/mitchellh/consul/${CONSUL_VERSION}_linux_amd64.zip && python -c "import zipfile; zipfile.ZipFile('${CONSUL_VERSION}_linux_amd64.zip').extractall('/usr/local/bin')" && chmod +x /usr/local/bin/consul && mkdir /etc/consul.d && rm ${CONSUL_VERSION}_linux_amd64.zip

COPY files /

ENTRYPOINT ["/usr/local/sbin/init"]
