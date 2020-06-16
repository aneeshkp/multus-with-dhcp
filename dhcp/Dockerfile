FROM alpine:latest

## Dockerfile author
MAINTAINER  Aneesh Puttur  <aneeshputtur@gmail.com> 

## Install packages
RUN apk --no-cache add dnsmasq \
    && echo "conf-dir=/etc/dnsmasq,*.conf" > /etc/dnsmasq.conf
RUN mkdir -p /var/lib/dnsmasq
RUN ["touch", "/var/lib/dnsmasq/dnsmasq.leasefile"]
RUN ["touch", "/etc/dnsmasq.d/dnsmasq.hostsfile"]
RUN ["touch","/var/log/dnsmasq.log"]

EXPOSE 67/udp 547/udp

COPY dnsmasq.conf /etc/dnsmasq.conf

VOLUME ["/etc/dnsmasq"]

ENTRYPOINT ["dnsmasq"]
CMD ["-p0","-d"]
