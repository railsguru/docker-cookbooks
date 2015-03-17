FROM railsguru/supervisor

MAINTAINER Andy Lo-A-Foe <andy.loafoe@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

# Workaround for PAM issue
RUN apt-get -y build-dep pam
RUN export CONFIGURE_OPTS=--disable-audit && cd /root && apt-get -b source pam && dpkg -i libpam-doc*.deb libpam-modules*.deb libpam-runtime*.deb libpam0g*.deb
