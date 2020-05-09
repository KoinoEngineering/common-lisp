FROM debian:latest
WORKDIR /usr/src/root
RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install git build-essential automake libcurl4-openssl-dev
RUN git clone -b release https://github.com/roswell/roswell.git .
RUN chmod -R 777 bootstrap
RUN sh bootstrap
RUN ./configure
RUN make
RUN make install
RUN ros setup
RUN ros run
