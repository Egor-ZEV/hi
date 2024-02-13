modules {
    ...
    ldap {
        # Параметры подключения к серверу OpenLDAP
        server = "ldap.example.com"
        identity = "cn=admin,dc=example,dc=com"
        password = "adminpassword"
        basedn = "dc=example,dc=com"
        filter = "(uid=%{Stripped-User-Name:-%{User-Name}})"
        tls = no
        start_tls = no
        tls_reqcert = never
        ...
    }
    ...
}
