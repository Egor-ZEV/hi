openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | CONTAINER_LOG_LEVEL = 3 (info)
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | Search service in CONTAINER_SERVICE_DIR = /container/service :
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | link /container/service/:ssl-tools/startup.sh to /container/run/startup/:ssl-tools
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | link /container/service/slapd/startup.sh to /container/run/startup/slapd
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | link /container/service/slapd/process.sh to /container/run/process/slapd/run
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | Environment files will be proccessed in this order : 
openldap_server  | Caution: previously defined variables will not be overriden.
openldap_server  | /container/environment/99-default/default.yaml
openldap_server  | /container/environment/99-default/default.startup.yaml
openldap_server  | 
openldap_server  | To see how this files are processed and environment variables values,
openldap_server  | run this container with '--loglevel debug'
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | Running /container/run/startup/:ssl-tools...
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | Running /container/run/startup/slapd...
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | openldap user and group adjustments
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | get current openldap uid/gid info inside container
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | -------------------------------------
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | openldap GID/UID
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | -------------------------------------
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | User uid: 911
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | User gid: 911
openldap_server  | ***  INFO   | 2024-02-12 07:08:05 | uid/gid changed: false
openldap_server  | ***  INFO   | 2024-02-12 07:08:06 | -------------------------------------
openldap_server  | ***  INFO   | 2024-02-12 07:08:06 | updating file uid/gid ownership
ldap_ui          | [2024-02-12 07:08:06 +0000] [8] [INFO] Running on http://0.0.0.0:5000 (CTRL + C to quit)
openldap_server  | ***  INFO   | 2024-02-12 07:08:09 | Database and config directory are empty...
openldap_server  | ***  INFO   | 2024-02-12 07:08:09 | Init new ldap server...
openldap_server  |   Backing up /etc/ldap/slapd.d in /var/backups/slapd-2.4.57+dfsg-1~bpo10+1... done.
openldap_server  |   Creating initial configuration... done.
openldap_server  |   Creating LDAP directory... done.
openldap_server  | invoke-rc.d: could not determine current runlevel
openldap_server  | invoke-rc.d: policy-rc.d denied execution of restart.
openldap_server  | ***  INFO   | 2024-02-12 07:08:11 | Start OpenLDAP...
openldap_server  | ***  INFO   | 2024-02-12 07:08:12 | Waiting for OpenLDAP to start...
openldap_server  | ***  INFO   | 2024-02-12 07:08:12 | Add bootstrap schemas...
openldap_server  | config file testing succeeded
openldap_server  | ***  INFO   | 2024-02-12 07:08:13 | Add image bootstrap ldif...
openldap_server  | ***  INFO   | 2024-02-12 07:08:13 | Add custom bootstrap ldif...
openldap_server  | ***  INFO   | 2024-02-12 07:08:13 | Add TLS config...
openldap_server  | ***  INFO   | 2024-02-12 07:08:13 | No certificate file and certificate key provided, generate:
openldap_server  | ***  INFO   | 2024-02-12 07:08:13 | /container/service/slapd/assets/certs/ldap.crt and /container/service/slapd/assets/certs/ldap.key
openldap_server  | 2024/02/12 07:08:13 [INFO] generate received request
openldap_server  | 2024/02/12 07:08:13 [INFO] received CSR
openldap_server  | 2024/02/12 07:08:13 [INFO] generating key: ecdsa-384
openldap_server  | 2024/02/12 07:08:13 [INFO] encoded CSR
openldap_server  | 2024/02/12 07:08:14 [INFO] signed certificate with serial number 299408744243332347328942838268438647371309743108
openldap_server  | ***  INFO   | 2024-02-12 07:08:14 | Link /container/service/:ssl-tools/assets/default-ca/default-ca.pem to /container/service/slapd/assets/certs/ca.crt
openldap_server  | ***  INFO   | 2024-02-12 07:08:14 | Disable replication config...
openldap_server  | ***  INFO   | 2024-02-12 07:08:14 | Stop OpenLDAP...
openldap_server  | ***  INFO   | 2024-02-12 07:08:14 | Configure ldap client TLS configuration...
openldap_server  | ***  INFO   | 2024-02-12 07:08:14 | Remove config files...
openldap_server  | ***  INFO   | 2024-02-12 07:08:14 | First start is done...
openldap_server  | ***  INFO   | 2024-02-12 07:08:14 | Remove file /container/environment/99-default/default.startup.yaml
openldap_server  | ***  INFO   | 2024-02-12 07:08:14 | Environment files will be proccessed in this order : 
openldap_server  | Caution: previously defined variables will not be overriden.
openldap_server  | /container/environment/99-default/default.yaml
openldap_server  | 
openldap_server  | To see how this files are processed and environment variables values,
openldap_server  | run this container with '--loglevel debug'
openldap_server  | ***  INFO   | 2024-02-12 07:08:14 | Running /container/run/process/slapd/run...
openldap_server  | 65c9c3de @(#) $OpenLDAP: slapd 2.4.57+dfsg-1~bpo10+1 (Jan 30 2021 06:59:51) $
openldap_server  | 	Debian OpenLDAP Maintainers <pkg-openldap-devel@lists.alioth.debian.org>
openldap_server  | 65c9c3de slapd starting
openldap_server  | 65c9c3f3 conn=1000 fd=12 ACCEPT from IP=172.28.0.3:45276 (IP=0.0.0.0:389)
openldap_server  | 65c9c3f3 conn=1000 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap_server  | 65c9c3f3 conn=1000 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui          | [2024-02-12 07:08:35 +0000] [8] [INFO] 172.28.0.1:40970 - - [12/Feb/2024:07:08:35 +0000] "GET /api/whoami 1.1" 500 127 "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui          | [2024-02-12 07:08:35 +0000] [8] [INFO] 172.28.0.1:40970 - - [12/Feb/2024:07:08:35 +0000] "GET /api/whoami 1.1" - - "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
openldap_server  | 65c9c3f3 conn=1001 fd=13 ACCEPT from IP=172.28.0.3:45280 (IP=0.0.0.0:389)
openldap_server  | 65c9c3f3 conn=1001 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap_server  | 65c9c3f3 conn=1001 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui          | [2024-02-12 07:08:35 +0000] [8] [INFO] 172.28.0.1:40970 - - [12/Feb/2024:07:08:35 +0000] "GET /api/schema 1.1" 500 127 "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui          | [2024-02-12 07:08:35 +0000] [8] [INFO] 172.28.0.1:40970 - - [12/Feb/2024:07:08:35 +0000] "GET /api/schema 1.1" - - "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
