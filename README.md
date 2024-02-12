version: '3'
services:
  openldap:
    image: osixia/openldap:latest
    container_name: openldap_server
    ports:
      - "389:389"
    environment:
      LDAP_ORGANISATION: "organization"
      LDAP_DOMAIN: "ldap.server.rlik"
      LDAP_ADMIN_PASSWORD: "admin"
    networks:
      - testnet

  openldap-ui:
    image: dnknth/ldap-ui:latest 
    container_name: ldap_ui
    ports:
      - "5000:5000"
    environment:
      LDAP_URL: 
      BASE_DN: "dc=ldap,dc=server,dc=rlik"
    networks:
      - testnet


networks:
  testnet:
    ipam:
      driver: default
      config:
        - subnet: 172.28.0.0/16
