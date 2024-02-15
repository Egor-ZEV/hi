ldap {
    server = "ldap://openldap"
    identity = "cn=admin,dc=MyCompany,dc=ldap,dc=server,dc=rlik"
    password = "admin"
    basedn = "dc=MyCompany,dc=ldap,dc=server,dc=rlik"
    filter = "(uid=%{%{Stripped-User-Name}:-%{User-Name}})"
    base_filter = "(objectClass=radiusprofile)"
    access_attr = "dialupAccess"
    dictionary_mapping = ${confdir}/ldap.attrmap
}

authorize {
    preprocess
    suffix
    files
    ldap
}
