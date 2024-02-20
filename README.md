version: '3'

services:
  freeradius:
    image: freeradius/freeradius-server:latest
    ports:
      - "1812-1813:1812-1813/udp"
    volumes:
      - ./radius:/etc/freeradius
    environment:
      - RADIUS_NO_DAEMONIZE=yes
