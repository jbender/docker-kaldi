FROM debian:8
MAINTAINER Jonathan Bender <jlbender@gmail.com>

ONBUILD RUN apt-get update && \
            apt-get install -y g++ zlib1g-dev make automake libtool-bin git autoconf && \
            apt-get install -y subversion libatlas3-base bzip2 wget python2.7 && \
            ln -s /usr/bin/python2.7 /usr/bin/python && \
            ln -s -f bash /bin/sh

ONBUILD RUN git clone https://github.com/jbender/kaldi.git /kaldi --depth=1

ONBUILD RUN cd /kaldi/tools && make

ENTRYPOINT ["bin/sh"]
