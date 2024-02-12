➜  dockers ldapsearch -x -H ldap://localhost -b dc=mycompany,dc=com -D "cn=admin,dc=mycompany,dc=com" -w admin_password
# extended LDIF
#
# LDAPv3
# base <dc=mycompany,dc=com> with scope subtree
# filter: (objectclass=*)
# requesting: ALL
#

# mycompany.com
dn: dc=mycompany,dc=com
objectClass: top
objectClass: dcObject
objectClass: organization
o: My Company
dc: mycompany

# search result
search: 2
result: 0 Success

# numResponses: 2
# numEntries: 1
