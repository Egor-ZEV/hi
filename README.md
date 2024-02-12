docker exec -it openldap /bin/bash
ldappasswd -H ldap://localhost -x -D "cn=admin,dc=example,dc=com" -W -S

