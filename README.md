version: '3'

services:
  openldap:
    image: osixia/openldap:1.5.0
    container_name: openldap
    environment:
      LDAP_ORGANISATION: "MyCompany"
      LDAP_DOMAIN: "ldap.server.rlik"
      LDAP_ADMIN_PASSWORD: "admin"
    ports:
      - "389:389"
    networks:
      - ldap_network

  ldap_ui:
    image: dnknth/ldap-ui
    container_name: ldap_ui
    environment:
      LDAP_URL: "ldap://openldap:389/"
      BASE_DN: "dc=ldap,dc=server,dc=rlik"
    ports:
      - "5000:5000"
    networks:
      - ldap_network

networks:
  ldap_network:
