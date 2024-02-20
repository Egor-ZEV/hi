version: '3'

services:
  openldap:
    image: osixia/openldap
    container_name: openldap
    environment:
      LDAP_ORGANISATION: "My Company"
      LDAP_DOMAIN: "example.com"
      LDAP_ADMIN_PASSWORD: "admin_password"
    ports:
      - "389:389"
      - "636:636"
  
  freeradius:
    image: freeradius/freeradius-server
    container_name: freeradius
    environment:
      RADIUS_CLIENTS: "localhost 0.0.0.0/0"
    ports:
      - "1812:1812/udp"
      - "1813:1813/udp"
    depends_on:
      - openldap
    command: ["freeradius", "-f", "-X", "-xx"]
    volumes:
      - ./certs:/etc/raddb/certs
      - ./mods-available:/etc/raddb/mods-available
      - ./sites-available:/etc/raddb/sites-available
      - ./clients.conf:/etc/raddb/clients.conf
