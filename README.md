FROM freeradius/freeradius-server

RUN apt-get update \
    && apt-get install -y wget build-essential libgnutls28-dev \
    && rm -rf /var/lib/apt/lists/*

RUN wget ftp://ftp.freeradius.org/pub/freeradius/freeradius-server-x.x.x.tar.gz \
    && tar -zxvf freeradius-server-x.x.x.tar.gz \
    && cd freeradius-server-x.x.x \
    && ./configure --with-openssl=no --with-gnutls=yes \
    && make \
    && make install

CMD ["radiusd", "-X"]
curl -s https://github.com/FreeRADIUS/freeradius-server/releases/latest | grep -o -E "v[0-9]+\.[0-9]+\.[0-9]+"
FROM freeradius/freeradius-server:v3.0.21
