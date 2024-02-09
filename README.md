version: '3'
services:
  openldap:
    image: osixia/openldap:latest
    container_name: openldap_server
    ports:
      - "389:389"
    environment:
      LDAP_ORGANISATION: "organization"
      LDAP_DOMAIN: "example.org"
      LDAP_ADMIN_PASSWORD: "admin"
