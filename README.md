version: '3'

services:
  openldap:
    image: osixia/openldap:latest
    container_name: openldap
    volumes:
      - /home/uic/Project/new/temp/openldap/data/:/var/lib/ldap
      - /home/uic/Project/new/temp/openldap/ldap.d/:/etc/ldap/slapd.d
    environment:
      LDAP_TLS: "false"
      LDAP_ORGANISATION: "MyCompany"
      LDAP_DOMAIN: "ldap.server.rlik"
      LDAP_ADMIN_PASSWORD: "admin"
      LDAP_CONFIG_PASSWORD: "admin"
    ports:
      - "389:389"
    networks:
      ldap_network:
        ipv4_address: 172.28.0.5

  phpldapadmin:
    image: osixia/phpldapadmin:latest
    container_name: phpldapadmin
    environment:
      PHPLDAPADMIN_LDAP_HOSTS: openldap
      PHPLDAPADMIN_HTTPS: "false"
    ports:
      - "7777:80"
    networks:
      ldap_network:
        ipv4_address: 172.28.0.8

  radius:
    image: freeradius/freeradius-server:latest
    container_name: radius
    environment:
      RADIUS_LDAP: |
        ldap {
          server = "openldap"
          identity = "cn=admin,dc=mycompany,dc=com"
          password = "admin"
          basedn = "dc=mycompany,dc=com"
          filter = "(uid=%{Stripped-User-Name:-%{User-Name}})"
          base_filter = "(objectClass=radiusprofile)"
          tls {
            start_tls = no
          }
        }
    ports:
      - "1812:1812/udp"
    networks:
      ldap_network:
        ipv4_address: 172.28.0.10

networks:
  ldap_network:
    ipam:
      driver: default
      config:
        - subnet: 172.28.0.0/16

