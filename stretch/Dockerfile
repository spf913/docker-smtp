FROM iloveuodi/stretch-slim

# Install exim4
ENV DEBIAN_FRONTEND noninteractive
ADD exim4-daemon-light.tar /
WORKDIR /exim4-daemon-light
RUN dpkg -i *.deb

COPY docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh
EXPOSE 25/tcp
ENTRYPOINT [ "docker-entrypoint.sh" ]
CMD [ "exim", "-bdf", "-v", "-q30m" ]
