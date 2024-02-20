FROM freeradius/freeradius-server

RUN apt-get update \
    && apt-get install -y libgnutls28-dev \
    && rm -rf /var/lib/apt/lists/*

RUN ./configure --with-openssl=no --with-gnutls=yes \
    && make \
    && make install


version: '3'

services:
  freeradius:
    build:
      context: .
      dockerfile: Dockerfile
    ports:
      - "1812:1812/udp"
      - "1813:1813/udp"
    volumes:
      - ./freeradius:/etc/freeradius
    environment:
      - RADIUS_CLIENTS=172.28.0.0/16
    command: radiusd -X
