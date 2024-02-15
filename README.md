version: '3'

services:
  openldap:
    # Ваши настройки для сервиса OpenLDAP
    ...

  phpldapadmin:
    # Ваши настройки для сервиса phpldapadmin
    ...

  radius:
    image: freeradius/freeradius-server:latest
    container_name: radius
    environment:
      RADIUS_LDAP_SERVERS: openldap
      RADIUS_LDAP_BIND_USER_DN: "cn=admin,dc=mycompany,dc=com"
      RADIUS_LDAP_BIND_PASSWORD: "admin"
      RADIUS_LDAP_USER_BASE_DN: "ou=users,dc=mycompany,dc=com"
      RADIUS_LDAP_GROUP_BASE_DN: "ou=groups,dc=mycompany,dc=com"
      RADIUS_LDAP_PROFILE: "ou=profiles,dc=mycompany,dc=com"
      RADIUS_LDAP_USERNAME_ATTRIBUTE: "uid"
      RADIUS_LDAP_GROUP_MEMBERSHIP: "cn"
    ports:
      - "1812:1812/udp"
    networks:
      - ldap_network

networks:
  ldap_network:
    external: true
