version: '3.7'

services:
  openldap:
    image: osixia/openldap:1.5.0
    environment:
      LDAP_ORGANISATION: "My Company"
      LDAP_DOMAIN: "example.com"
      LDAP_ADMIN_PASSWORD: "admin_password"
    networks:
      - ldap_network

  ldapui:
    image: dinkel/openldap-admin:latest
    environment:
      LDAP_HOST: openldap
      LDAP_PORT: 389
      LDAP_SECURE: "false"
    ports:
      - "8090:8080"
    networks:
      - ldap_network

networks:
  ldap_network:
    driver: bridge
