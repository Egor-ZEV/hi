ldap_ui   | [2024-02-12 11:59:58 +0000] [8] [INFO] 172.20.0.1:38976 - - [12/Feb/2024:11:59:58 +0000] "GET / 1.1" 304 - "-" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:59:58 +0000] [8] [INFO] 172.20.0.1:38976 - - [12/Feb/2024:11:59:58 +0000] "GET / 1.1" - - "-" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:59:58 +0000] [8] [INFO] 172.20.0.1:38976 - - [12/Feb/2024:11:59:58 +0000] "GET /api/whoami 1.1" 500 127 "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:59:58 +0000] [8] [INFO] 172.20.0.1:38976 - - [12/Feb/2024:11:59:58 +0000] "GET /api/whoami 1.1" - - "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
openldap  | 65ca083e conn=1018 fd=13 ACCEPT from IP=172.20.0.3:60848 (IP=0.0.0.0:389)
openldap  | 65ca083e conn=1018 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap  | 65ca083e conn=1018 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
openldap  | 65ca083e conn=1019 fd=14 ACCEPT from IP=172.20.0.3:60850 (IP=0.0.0.0:389)
openldap  | 65ca083e conn=1019 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap  | 65ca083e conn=1019 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui   | [2024-02-12 11:59:58 +0000] [8] [INFO] 172.20.0.1:38976 - - [12/Feb/2024:11:59:58 +0000] "GET /api/schema 1.1" 500 127 "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:59:58 +0000] [8] [INFO] 172.20.0.1:38976 - - [12/Feb/2024:11:59:58 +0000] "GET /api/schema 1.1" - - "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
