version: '3.8'

services:
  openldap:
    image: osixia/openldap:1.5.0
    environment:
      LDAP_ORGANISATION: "MyCompany"
      LDAP_DOMAIN: "example.com"
      LDAP_ADMIN_PASSWORD: "adminpassword"
    ports:
      - "389:389"
    networks:
      - ldap_network

  phpldapadmin:
    image: osixia/phpldapadmin:0.9.0
    environment:
      PHPLDAPADMIN_LDAP_HOSTS: "openldap"
      PHPLDAPADMIN_HTTPS: "false"
    ports:
      - "8080:80"
    networks:
      - ldap_network

networks:
  ldap_network:

