openldap  | 65ca04f5 conn=1000 fd=12 ACCEPT from IP=172.20.0.3:55274 (IP=0.0.0.0:389)
openldap  | 65ca04f5 conn=1000 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap  | 65ca04f5 conn=1000 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui   | [2024-02-12 11:45:57 +0000] [8] [INFO] 172.20.0.1:44918 - - [12/Feb/2024:11:45:57 +0000] "GET /api/whoami 1.1" 500 127 "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:45:57 +0000] [8] [INFO] 172.20.0.1:44918 - - [12/Feb/2024:11:45:57 +0000] "GET /api/whoami 1.1" - - "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
openldap  | 65ca04f5 conn=1001 fd=13 ACCEPT from IP=172.20.0.3:55278 (IP=0.0.0.0:389)
openldap  | 65ca04f5 conn=1001 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap  | 65ca04f5 conn=1001 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui   | [2024-02-12 11:45:57 +0000] [8] [INFO] 172.20.0.1:44918 - - [12/Feb/2024:11:45:57 +0000] "GET /api/schema 1.1" 500 127 "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:45:57 +0000] [8] [INFO] 172.20.0.1:44918 - - [12/Feb/2024:11:45:57 +0000] "GET /api/schema 1.1" - - "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"

