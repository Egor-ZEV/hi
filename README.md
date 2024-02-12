version: '3'

services:
  openldap:
    image: osixia/openldap:1.5.0
    container_name: openldap
    environment:
      LDAP_ORGANISATION: "MyCompany"
      LDAP_DOMAIN: "ldap.server.rlik"
      LDAP_ADMIN_PASSWORD: "adminpassword"
    ports:
      - "389:389"
    networks:
      - ldap_network

  ldap_ui:
    image: dnknth/ldap-ui
    container_name: ldap_ui
    environment:
      - LDAP_URL=ldap://openldap/
      - BASE_DN=dc=ldap,dc=server,dc=rlik
    ports:
      - "5000:5000"
    networks:
      - ldap_network

  radius:
    image: freeradius/freeradius-server:latest
    container_name: radius
    ports:
      - "1812:1812/udp"
    networks:
      - ldap_network

networks:
  ldap_network:
