FROM ubuntu:16.04
RUN apt update \
  && apt-get install -y globus-gridftp-server-progs globus-gass-copy-progs
CMD globus-gridftp-server -c /etc/gridftp.conf
