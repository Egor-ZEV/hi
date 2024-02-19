version: '3'

services:
  freeradius:
    image: freeradius/freeradius-server:latest
    ports:
      - "1812:1812/udp"
      - "1813:1813/udp"
    volumes:
      - /path/to/freeradius/config:/etc/freeradius
      - /path/to/freeradius/logs:/var/log/freeradius
    restart: always
