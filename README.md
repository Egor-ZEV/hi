openldap  | 65ca073d conn=1009 fd=14 ACCEPT from IP=172.20.0.1:38566 (IP=0.0.0.0:389)
openldap  | 65ca073d conn=1009 op=0 BIND dn="cn=admin,dc=ldap,dc=server,dc=rlik" method=128
openldap  | 65ca073d conn=1009 op=0 BIND dn="cn=admin,dc=ldap,dc=server,dc=rlik" mech=SIMPLE ssf=0
openldap  | 65ca073d conn=1009 op=0 RESULT tag=97 err=0 text=
openldap  | 65ca073d conn=1009 op=1 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(objectClass=*)"
openldap  | 65ca073d conn=1009 op=1 SEARCH RESULT tag=101 err=0 nentries=1 text=
openldap  | 65ca073d conn=1009 op=2 UNBIND
openldap  | 65ca073d conn=1009 fd=14 closed
