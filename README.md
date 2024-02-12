openldap  | ***  INFO   | 2024-02-12 11:27:07 | CONTAINER_LOG_LEVEL = 3 (info)
openldap  | ***  INFO   | 2024-02-12 11:27:07 | Search service in CONTAINER_SERVICE_DIR = /container/service :
openldap  | ***  INFO   | 2024-02-12 11:27:07 | link /container/service/:ssl-tools/startup.sh to /container/run/startup/:ssl-tools
openldap  | ***  INFO   | 2024-02-12 11:27:07 | link /container/service/slapd/startup.sh to /container/run/startup/slapd
openldap  | ***  INFO   | 2024-02-12 11:27:07 | link /container/service/slapd/process.sh to /container/run/process/slapd/run
openldap  | ***  INFO   | 2024-02-12 11:27:07 | Environment files will be proccessed in this order : 
openldap  | Caution: previously defined variables will not be overriden.
openldap  | /container/environment/99-default/default.yaml
openldap  | /container/environment/99-default/default.startup.yaml
openldap  | 
openldap  | To see how this files are processed and environment variables values,
openldap  | run this container with '--loglevel debug'
openldap  | ***  INFO   | 2024-02-12 11:27:07 | Running /container/run/startup/:ssl-tools...
openldap  | ***  INFO   | 2024-02-12 11:27:07 | Running /container/run/startup/slapd...
openldap  | ***  INFO   | 2024-02-12 11:27:07 | openldap user and group adjustments
openldap  | ***  INFO   | 2024-02-12 11:27:07 | get current openldap uid/gid info inside container
openldap  | ***  INFO   | 2024-02-12 11:27:07 | -------------------------------------
openldap  | ***  INFO   | 2024-02-12 11:27:07 | openldap GID/UID
openldap  | ***  INFO   | 2024-02-12 11:27:07 | -------------------------------------
openldap  | ***  INFO   | 2024-02-12 11:27:07 | User uid: 911
openldap  | ***  INFO   | 2024-02-12 11:27:07 | User gid: 911
openldap  | ***  INFO   | 2024-02-12 11:27:07 | uid/gid changed: false
openldap  | ***  INFO   | 2024-02-12 11:27:07 | -------------------------------------
openldap  | ***  INFO   | 2024-02-12 11:27:07 | updating file uid/gid ownership
ldap_ui   | [2024-02-12 11:27:08 +0000] [8] [INFO] Running on http://0.0.0.0:5000 (CTRL + C to quit)
openldap  | ***  INFO   | 2024-02-12 11:27:11 | Database and config directory are empty...
openldap  | ***  INFO   | 2024-02-12 11:27:11 | Init new ldap server...
openldap  |   Backing up /etc/ldap/slapd.d in /var/backups/slapd-2.4.57+dfsg-1~bpo10+1... done.
openldap  |   Creating initial configuration... done.
openldap  |   Creating LDAP directory... done.
openldap  | invoke-rc.d: could not determine current runlevel
openldap  | invoke-rc.d: policy-rc.d denied execution of restart.
openldap  | ***  INFO   | 2024-02-12 11:27:14 | Start OpenLDAP...
openldap  | ***  INFO   | 2024-02-12 11:27:14 | Waiting for OpenLDAP to start...
openldap  | ***  INFO   | 2024-02-12 11:27:14 | Add bootstrap schemas...
openldap  | config file testing succeeded
openldap  | ***  INFO   | 2024-02-12 11:27:15 | Add image bootstrap ldif...
openldap  | ***  INFO   | 2024-02-12 11:27:16 | Add custom bootstrap ldif...
openldap  | ***  INFO   | 2024-02-12 11:27:16 | Add TLS config...
openldap  | ***  INFO   | 2024-02-12 11:27:16 | No certificate file and certificate key provided, generate:
openldap  | ***  INFO   | 2024-02-12 11:27:16 | /container/service/slapd/assets/certs/ldap.crt and /container/service/slapd/assets/certs/ldap.key
openldap  | 2024/02/12 11:27:16 [INFO] generate received request
openldap  | 2024/02/12 11:27:16 [INFO] received CSR
openldap  | 2024/02/12 11:27:16 [INFO] generating key: ecdsa-384
openldap  | 2024/02/12 11:27:16 [INFO] encoded CSR
openldap  | 2024/02/12 11:27:16 [INFO] signed certificate with serial number 717844877662584605887789023156577588549518007376
openldap  | ***  INFO   | 2024-02-12 11:27:16 | Link /container/service/:ssl-tools/assets/default-ca/default-ca.pem to /container/service/slapd/assets/certs/ca.crt
openldap  | ***  INFO   | 2024-02-12 11:27:17 | Disable replication config...
openldap  | ***  INFO   | 2024-02-12 11:27:17 | Stop OpenLDAP...
openldap  | ***  INFO   | 2024-02-12 11:27:17 | Configure ldap client TLS configuration...
openldap  | ***  INFO   | 2024-02-12 11:27:17 | Remove config files...
openldap  | ***  INFO   | 2024-02-12 11:27:17 | First start is done...
openldap  | ***  INFO   | 2024-02-12 11:27:17 | Remove file /container/environment/99-default/default.startup.yaml
openldap  | ***  INFO   | 2024-02-12 11:27:17 | Environment files will be proccessed in this order : 
openldap  | Caution: previously defined variables will not be overriden.
openldap  | /container/environment/99-default/default.yaml
openldap  | 
openldap  | To see how this files are processed and environment variables values,
openldap  | run this container with '--loglevel debug'
openldap  | ***  INFO   | 2024-02-12 11:27:17 | Running /container/run/process/slapd/run...
openldap  | 65ca0095 @(#) $OpenLDAP: slapd 2.4.57+dfsg-1~bpo10+1 (Jan 30 2021 06:59:51) $
openldap  | 	Debian OpenLDAP Maintainers <pkg-openldap-devel@lists.alioth.debian.org>
openldap  | 65ca0095 slapd starting
openldap  | 65ca00a6 conn=1000 fd=12 ACCEPT from IP=172.20.0.3:54886 (IP=0.0.0.0:389)
openldap  | 65ca00a6 conn=1000 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap  | 65ca00a6 conn=1000 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui   | [2024-02-12 11:27:34 +0000] [8] [INFO] 172.20.0.1:59912 - - [12/Feb/2024:11:27:34 +0000] "GET /favicon.ico 1.1" 200 4286 "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:27:34 +0000] [8] [INFO] 172.20.0.1:59912 - - [12/Feb/2024:11:27:34 +0000] "GET /favicon.ico 1.1" - - "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:27:34 +0000] [8] [INFO] 172.20.0.1:59900 - - [12/Feb/2024:11:27:34 +0000] "GET /api/whoami 1.1" 500 127 "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:27:34 +0000] [8] [INFO] 172.20.0.1:59900 - - [12/Feb/2024:11:27:34 +0000] "GET /api/whoami 1.1" - - "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
openldap  | 65ca00a6 conn=1001 fd=13 ACCEPT from IP=172.20.0.3:54902 (IP=0.0.0.0:389)
openldap  | 65ca00a6 conn=1001 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap  | 65ca00a6 conn=1001 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui   | [2024-02-12 11:27:34 +0000] [8] [INFO] 172.20.0.1:59900 - - [12/Feb/2024:11:27:34 +0000] "GET /api/schema 1.1" 500 127 "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:27:34 +0000] [8] [INFO] 172.20.0.1:59900 - - [12/Feb/2024:11:27:34 +0000] "GET /api/schema 1.1" - - "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
openldap  | 65ca00a6 conn=1000 op=1 UNBIND
openldap  | 65ca00a6 conn=1000 fd=12 closed
ldap_ui   | [2024-02-12 11:27:46 +0000] [8] [INFO] 172.20.0.1:33614 - - [12/Feb/2024:11:27:46 +0000] "GET / 1.1" 304 - "-" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:27:46 +0000] [8] [INFO] 172.20.0.1:33614 - - [12/Feb/2024:11:27:46 +0000] "GET / 1.1" - - "-" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
openldap  | 65ca00b2 conn=1002 fd=12 ACCEPT from IP=172.20.0.3:56352 (IP=0.0.0.0:389)
openldap  | 65ca00b2 conn=1002 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap  | 65ca00b2 conn=1002 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui   | [2024-02-12 11:27:46 +0000] [8] [INFO] 172.20.0.1:33614 - - [12/Feb/2024:11:27:46 +0000] "GET /api/whoami 1.1" 500 127 "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:27:46 +0000] [8] [INFO] 172.20.0.1:33614 - - [12/Feb/2024:11:27:46 +0000] "GET /api/whoami 1.1" - - "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
openldap  | 65ca00b2 conn=1003 fd=14 ACCEPT from IP=172.20.0.3:56368 (IP=0.0.0.0:389)
openldap  | 65ca00b2 conn=1003 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap  | 65ca00b2 conn=1003 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui   | [2024-02-12 11:27:46 +0000] [8] [INFO] 172.20.0.1:33614 - - [12/Feb/2024:11:27:46 +0000] "GET /api/schema 1.1" 500 127 "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:27:46 +0000] [8] [INFO] 172.20.0.1:33614 - - [12/Feb/2024:11:27:46 +0000] "GET /api/schema 1.1" - - "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
