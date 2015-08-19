FROM jbender/kaldi-base
MAINTAINER Jonathan Bender <jlbender@gmail.com>

RUN cd /kaldi/src && ./configure && make depend && make

ENTRYPOINT ["bin/sh"]
