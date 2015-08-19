FROM debian:8
MAINTAINER Jonathan Bender <jlbender@gmail.com>

RUN apt-get update && \
    apt-get install -y g++ zlib1g-dev make automake libtool-bin git autoconf && \
    apt-get install -y subversion libatlas3-base bzip2 wget python2.7 && \
    ln -s /usr/bin/python2.7 /usr/bin/python && \
    ln -s -f bash /bin/sh

RUN git clone https://github.com/jbender/kaldi.git /kaldi --depth=1
RUN cd /kaldi/tools && make
RUN cd /kaldi/src && ./configure --shared && make depend && make

ENTRYPOINT ["bin/sh"]
