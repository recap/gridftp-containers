FROM ubuntu:16.04
RUN apt update \
  && apt-get install -y globus-gridftp-server-progs globus-gass-copy-progs
CMD globus-url-copy -vb -p 10 $SRC $DST
