version: '3'

services:
  openldap:
    image: osixia/openldap
    environment:
      LDAP_ORGANISATION: "My Company"
      LDAP_DOMAIN: "mycompany.com"
      LDAP_ADMIN_PASSWORD: "admin_password"
    ports:
      - "389:389"
      - "636:636"
    networks:
      - ldap_network

  phpldapadmin:
    image: osixia/phpldapadmin
    environment:
      PHPLDAPADMIN_LDAP_HOSTS: "openldap"
      PHPLDAPADMIN_HTTPS: "false"
    ports:
      - "8080:80"
    networks:
      - ldap_network

  ldapadmin:
    image: dinkel/phpldapadmin
    environment:
      LDAP_HOSTS: "openldap"
    ports:
      - "8081:80"
    networks:
      - ldap_network

  ldap-account-manager:
    image: ldapaccountmanager/lam
    environment:
      LAM_PASSWORD_HASH: "SSHA"
      LAM_APP_PASSWORD_HASH: "SSHA"
      LDAP_HOSTS: "openldap"
    ports:
      - "8082:80"
    networks:
      - ldap_network

  apache-ds:
    image: apachedirectorystudio/apacheds
    ports:
      - "8083:80"
    networks:
      - ldap_network

  ldap-browser:
    image: jtgasper3/ldapbrowser
    environment:
      LDAP_SERVER: "openldap"
    ports:
      - "8084:80"
    networks:
      - ldap_network

networks:
  ldap_network:
