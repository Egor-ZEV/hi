root@cf649877b739:/etc/freeradius/mods-enabled# ldapsearch -x -H ldap://ldap.server.rlik:389 -b dc=ldap,dc=server,dc=rlik -D "cn=admin,dc=ldap,dc=server,dc=rlik" -w admin
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
o: MyCompany
dc: ldap

# ops, ldap.server.rlik
dn: cn=ops,dc=ldap,dc=server,dc=rlik
cn: ops
gidNumber: 500
objectClass: posixGroup
objectClass: top

# test, ops, ldap.server.rlik
dn: cn=test,cn=ops,dc=ldap,dc=server,dc=rlik
givenName: test
sn: test
cn: test
uid: test
userPassword:: e01ENX1DWTlyelVZaDAzUEszazZESmllMDlnPT0=
uidNumber: 1000
gidNumber: 500
homeDirectory: /home/users/test
objectClass: inetOrgPerson
objectClass: posixAccount
objectClass: top

# test1 test1, ldap.server.rlik
dn: cn=test1 test1,dc=ldap,dc=server,dc=rlik
givenName: test1
sn: test1
cn: test1 test1
uid: ttest1
userPassword:: e01ENX1XaEJlaTUxQTRUS1hnTll1b2laZGlnPT0=
uidNumber: 1001
gidNumber: 500
homeDirectory: /home/users/ttest1
objectClass: inetOrgPerson
objectClass: posixAccount
objectClass: top

# search result
search: 2
result: 0 Success

# numResponses: 5
# numEntries: 4
