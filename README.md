version: '3'

services:
  openldap:
    image: osixia/openldap:1.5.0
    environment:
      LDAP_ORGANISATION: "My Company"
      LDAP_DOMAIN: "example.com"
      LDAP_ADMIN_PASSWORD: "admin_password"
    ports:
      - "389:389"
    networks:
      - ldap-network
    volumes:
      - ldap-data:/var/lib/ldap
      - ldap-config:/etc/ldap/slapd.d

  phpldapadmin:
    image: osixia/phpldapadmin:0.9.0
    environment:
      PHPLDAPADMIN_LDAP_HOSTS: "openldap"
    ports:
      - "8080:80"
    networks:
      - ldap-network

networks:
  ldap-network:

volumes:
  ldap-data:
  ldap-config:
