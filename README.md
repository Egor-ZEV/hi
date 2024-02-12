openldap-1 exited with code 0
openldap-1 has been recreated
openldap-1 exited with code 0
openldap-1 has been recreated
openldap-1      | ***  INFO   | 2024-02-12 10:08:10 | CONTAINER_LOG_LEVEL = 3 (info)
openldap-1      | ***  INFO   | 2024-02-12 10:08:10 | Search service in CONTAINER_SERVICE_DIR = /container/service :
openldap-1      | ***  INFO   | 2024-02-12 10:08:10 | link /container/service/:ssl-tools/startup.sh to /container/run/startup/:ssl-tools
openldap-1      | ***  INFO   | 2024-02-12 10:08:10 | link /container/service/slapd/startup.sh to /container/run/startup/slapd
openldap-1      | ***  INFO   | 2024-02-12 10:08:10 | link /container/service/slapd/process.sh to /container/run/process/slapd/run
openldap-1      | ***  INFO   | 2024-02-12 10:08:10 | Environment files will be proccessed in this order : 
openldap-1      | Caution: previously defined variables will not be overriden.
openldap-1      | /container/environment/99-default/default.yaml
openldap-1      | /container/environment/99-default/default.startup.yaml
openldap-1      | 
openldap-1      | To see how this files are processed and environment variables values,
openldap-1      | run this container with '--loglevel debug'
openldap-1      | ***  INFO   | 2024-02-12 10:08:10 | Running /container/run/startup/:ssl-tools...
openldap-1      | ***  INFO   | 2024-02-12 10:08:11 | Running /container/run/startup/slapd...
openldap-1      | ***  INFO   | 2024-02-12 10:08:11 | openldap user and group adjustments
openldap-1      | ***  INFO   | 2024-02-12 10:08:11 | get current openldap uid/gid info inside container
openldap-1      | ***  INFO   | 2024-02-12 10:08:11 | -------------------------------------
openldap-1      | ***  INFO   | 2024-02-12 10:08:11 | openldap GID/UID
openldap-1      | ***  INFO   | 2024-02-12 10:08:11 | -------------------------------------
openldap-1      | ***  INFO   | 2024-02-12 10:08:11 | User uid: 911
openldap-1      | ***  INFO   | 2024-02-12 10:08:11 | User gid: 911
openldap-1      | ***  INFO   | 2024-02-12 10:08:11 | uid/gid changed: false
openldap-1      | ***  INFO   | 2024-02-12 10:08:11 | -------------------------------------
openldap-1      | ***  INFO   | 2024-02-12 10:08:11 | updating file uid/gid ownership
openldap-1      | ***  INFO   | 2024-02-12 10:08:14 | Database and config directory are empty...
openldap-1      | ***  INFO   | 2024-02-12 10:08:14 | Init new ldap server...
openldap-1      |   Backing up /etc/ldap/slapd.d in /var/backups/slapd-2.4.57+dfsg-1~bpo10+1... done.
openldap-1      |   Creating initial configuration... done.
openldap-1      |   Creating LDAP directory... done.
openldap-1      | invoke-rc.d: could not determine current runlevel
openldap-1      | invoke-rc.d: policy-rc.d denied execution of restart.
openldap-1      | ***  INFO   | 2024-02-12 10:08:16 | Start OpenLDAP...
openldap-1      | ***  INFO   | 2024-02-12 10:08:16 | Waiting for OpenLDAP to start...
openldap-1      | ***  INFO   | 2024-02-12 10:08:16 | Add bootstrap schemas...
openldap-1      | config file testing succeeded
openldap-1      | ***  INFO   | 2024-02-12 10:08:17 | Add image bootstrap ldif...
openldap-1      | ***  INFO   | 2024-02-12 10:08:18 | Add custom bootstrap ldif...
openldap-1      | ***  INFO   | 2024-02-12 10:08:18 | Add TLS config...
openldap-1      | ***  INFO   | 2024-02-12 10:08:18 | No certificate file and certificate key provided, generate:
openldap-1      | ***  INFO   | 2024-02-12 10:08:18 | /container/service/slapd/assets/certs/ldap.crt and /container/service/slapd/assets/certs/ldap.key
openldap-1      | 2024/02/12 10:08:18 [INFO] generate received request
openldap-1      | 2024/02/12 10:08:18 [INFO] received CSR
openldap-1      | 2024/02/12 10:08:18 [INFO] generating key: ecdsa-384
openldap-1      | 2024/02/12 10:08:18 [INFO] encoded CSR
openldap-1      | 2024/02/12 10:08:18 [INFO] signed certificate with serial number 583307963920993165206521155443417674868006853055
openldap-1      | ***  INFO   | 2024-02-12 10:08:19 | Link /container/service/:ssl-tools/assets/default-ca/default-ca.pem to /container/service/slapd/assets/certs/ca.crt
openldap-1      | ***  INFO   | 2024-02-12 10:08:19 | Disable replication config...
openldap-1      | ***  INFO   | 2024-02-12 10:08:19 | Stop OpenLDAP...
openldap-1      | ***  INFO   | 2024-02-12 10:08:19 | Configure ldap client TLS configuration...
openldap-1      | ***  INFO   | 2024-02-12 10:08:19 | Remove config files...
openldap-1      | ***  INFO   | 2024-02-12 10:08:19 | First start is done...
openldap-1      | ***  INFO   | 2024-02-12 10:08:19 | Remove file /container/environment/99-default/default.startup.yaml
openldap-1      | ***  INFO   | 2024-02-12 10:08:19 | Environment files will be proccessed in this order : 
openldap-1      | Caution: previously defined variables will not be overriden.
openldap-1      | /container/environment/99-default/default.yaml
openldap-1      | 
openldap-1      | To see how this files are processed and environment variables values,
openldap-1      | run this container with '--loglevel debug'
openldap-1      | ***  INFO   | 2024-02-12 10:08:19 | Running /container/run/process/slapd/run...
openldap-1      | 65c9ee13 @(#) $OpenLDAP: slapd 2.4.57+dfsg-1~bpo10+1 (Jan 30 2021 06:59:51) $
openldap-1      | 	Debian OpenLDAP Maintainers <pkg-openldap-devel@lists.alioth.debian.org>
openldap-1      | 65c9ee13 slapd starting
openldap-1      | 65c9ee23 conn=1000 fd=12 ACCEPT from IP=172.28.0.3:37316 (IP=0.0.0.0:389)
openldap-1      | 65c9ee23 conn=1000 op=0 do_bind: invalid dn (admin)
openldap-1      | 65c9ee23 conn=1000 op=0 RESULT tag=97 err=34 text=invalid DN
openldap-1      | 65c9ee23 conn=1000 op=1 UNBIND
openldap-1      | 65c9ee23 conn=1000 fd=12 closed
phpldapadmin-1  | 172.28.0.1 - - [12/Feb/2024:10:08:35 +0000] "POST /cmd.php HTTP/1.1" 302 473 "http://127.0.0.1:8080/cmd.php?cmd=login_form&server_id=1&redirect=true" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
phpldapadmin-1  | 172.28.0.1 - - [12/Feb/2024:10:08:35 +0000] "GET /cmd.php?cmd=login_form&server_id=1&redirect=true HTTP/1.1" 200 2303 "http://127.0.0.1:8080/cmd.php?cmd=login_form&server_id=1&redirect=true" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"

