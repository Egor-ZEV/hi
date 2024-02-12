➜  dockers ldapsearch -x -H ldap://localhost -b dc=ldap,dc=server,dc=rlik -D "cn=admin,dc=ldap,dc=server,dc=rlik" -w admin
# extended LDIF
#
# LDAPv3
# base <dc=ldap,dc=server,dc=rlik> with scope subtree
# filter: (objectclass=*)
# requesting: ALL
#

# ldap.server.rlik
dn: dc=ldap,dc=server,dc=rlik
objectClass: top
objectClass: dcObject
objectClass: organization
o: organization
dc: ldap

# search result
search: 2
result: 0 Success

# numResponses: 2
# numEntries: 1
