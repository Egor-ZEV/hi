ldap_ui          | [2024-02-09 09:42:20 +0000] [1] [INFO] 172.28.0.1:60250 - - [09/Feb/2024:09:42:20 +0000] "GET / 1.1" 200 820 "-" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
openldap_server  | 65c5f37c conn=1004 fd=12 ACCEPT from IP=172.28.0.2:42766 (IP=0.0.0.0:389)
openldap_server  | 65c5f37c conn=1004 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap_server  | 65c5f37c conn=1004 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui          | [2024-02-09 09:42:20 +0000] [1] [INFO] 172.28.0.1:60250 - - [09/Feb/2024:09:42:20 +0000] "GET /api/whoami 1.1" 500 127 "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
openldap_server  | 65c5f37c conn=1004 op=1 UNBIND
openldap_server  | 65c5f37c conn=1004 fd=12 closed
openldap_server  | 65c5f37c conn=1005 fd=12 ACCEPT from IP=172.28.0.2:42774 (IP=0.0.0.0:389)
ldap_ui          | [2024-02-09 09:42:20 +0000] [1] [INFO] 172.28.0.1:60250 - - [09/Feb/2024:09:42:20 +0000] "GET /api/schema 1.1" 500 127 "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
openldap_server  | 65c5f37c conn=1005 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap_server  | 65c5f37c conn=1005 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
openldap_server  | 65c5f37c conn=1005 op=1 UNBIND
openldap_server  | 65c5f37c conn=1005 fd=12 closed
