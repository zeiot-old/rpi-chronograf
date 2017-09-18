# VERSION 1.3.8.1
# AUTHOR:         Nicolas Lamirault <nicolas.lamirault@gmail.com>
# DESCRIPTION:    zeiot/rpi-chronograf

FROM resin/armv7hf-debian:jessie
MAINTAINER Nicolas Lamirault <nicolas.lamirault@gmail.com>

ENV CHRONOGRAF_VERSION 1.3.8.1

# TODO: https://github.com/moby/moby/issues/33849
# ADD https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_armhf.tar.gz /chronograf.tar.gz
RUN apt update && \
    apt install curl
RUN curl https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_armhf.tar.gz -o /chronograf.tar.gz \ 
    && tar -xf /chronograf.tar.gz \
    && rm /chronograf.tar.gz \
    && cp /chronograf-${CHRONOGRAF_VERSION}-*/usr/bin/chronograf /usr/bin/ \
    && cp -r /chronograf-${CHRONOGRAF_VERSION}-*/usr/lib/* /usr/lib/ \
    && cp -r /chronograf-${CHRONOGRAF_VERSION}-*/usr/share/* /usr/share/ \
    && cp -r /chronograf-${CHRONOGRAF_VERSION}-*/etc/* /etc/ \
    && mkdir /etc/chronograf /var/lib/chronograf /var/log/chronograf

EXPOSE     8888

VOLUME     [ "/usr/share/chronograf", "/var/lib/chronograf" ]

CMD        [ "/usr/bin/chronograf", "-b", "/var/lib/chronograf/chronograf-v1.db", "-c", "/usr/share/chronograf/canned" ]
