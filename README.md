version: '3'

services:
  openldap:
    image: osixia/openldap:1.5.0
    container_name: openldap
    environment:
      LDAP_ORGANISATION: "MyCompany"
      LDAP_DOMAIN: "ldap.server.rlik"
      LDAP_ADMIN_PASSWORD: "admin"
    ports:
      - "389:389"
    networks:
      - ldap_network

  ldap_ui:
    image: dnknth/ldap-ui
    container_name: ldap_ui
    environment:
      LDAP_URL: "ldap://openldap:389/"
      BASE_DN: "dc=ldap,dc=server,dc=rlik"
    ports:
      - "5000:5000"
    networks:
      - ldap_network

networks:
  ldap_network:
Attaching to ldap_ui, openldap
openldap  | ***  INFO   | 2024-02-12 11:33:39 | CONTAINER_LOG_LEVEL = 3 (info)
openldap  | ***  INFO   | 2024-02-12 11:33:39 | Search service in CONTAINER_SERVICE_DIR = /container/service :
openldap  | ***  INFO   | 2024-02-12 11:33:39 | link /container/service/:ssl-tools/startup.sh to /container/run/startup/:ssl-tools
openldap  | ***  INFO   | 2024-02-12 11:33:39 | link /container/service/slapd/startup.sh to /container/run/startup/slapd
openldap  | ***  INFO   | 2024-02-12 11:33:39 | link /container/service/slapd/process.sh to /container/run/process/slapd/run
openldap  | ***  INFO   | 2024-02-12 11:33:39 | Environment files will be proccessed in this order : 
openldap  | Caution: previously defined variables will not be overriden.
openldap  | /container/environment/99-default/default.yaml
openldap  | /container/environment/99-default/default.startup.yaml
openldap  | 
openldap  | To see how this files are processed and environment variables values,
openldap  | run this container with '--loglevel debug'
openldap  | ***  INFO   | 2024-02-12 11:33:39 | Running /container/run/startup/:ssl-tools...
openldap  | ***  INFO   | 2024-02-12 11:33:39 | Running /container/run/startup/slapd...
openldap  | ***  INFO   | 2024-02-12 11:33:39 | openldap user and group adjustments
openldap  | ***  INFO   | 2024-02-12 11:33:39 | get current openldap uid/gid info inside container
openldap  | ***  INFO   | 2024-02-12 11:33:39 | -------------------------------------
openldap  | ***  INFO   | 2024-02-12 11:33:39 | openldap GID/UID
openldap  | ***  INFO   | 2024-02-12 11:33:39 | -------------------------------------
openldap  | ***  INFO   | 2024-02-12 11:33:39 | User uid: 911
openldap  | ***  INFO   | 2024-02-12 11:33:39 | User gid: 911
openldap  | ***  INFO   | 2024-02-12 11:33:39 | uid/gid changed: false
openldap  | ***  INFO   | 2024-02-12 11:33:39 | -------------------------------------
openldap  | ***  INFO   | 2024-02-12 11:33:39 | updating file uid/gid ownership
ldap_ui   | [2024-02-12 11:33:41 +0000] [8] [INFO] Running on http://0.0.0.0:5000 (CTRL + C to quit)
openldap  | ***  INFO   | 2024-02-12 11:33:43 | Database and config directory are empty...
openldap  | ***  INFO   | 2024-02-12 11:33:43 | Init new ldap server...
openldap  |   Backing up /etc/ldap/slapd.d in /var/backups/slapd-2.4.57+dfsg-1~bpo10+1... done.
openldap  |   Creating initial configuration... done.
openldap  |   Creating LDAP directory... done.
openldap  | invoke-rc.d: could not determine current runlevel
openldap  | invoke-rc.d: policy-rc.d denied execution of restart.
openldap  | ***  INFO   | 2024-02-12 11:33:45 | Start OpenLDAP...
openldap  | ***  INFO   | 2024-02-12 11:33:45 | Waiting for OpenLDAP to start...
openldap  | ***  INFO   | 2024-02-12 11:33:45 | Add bootstrap schemas...
openldap  | config file testing succeeded
openldap  | ***  INFO   | 2024-02-12 11:33:46 | Add image bootstrap ldif...
openldap  | ***  INFO   | 2024-02-12 11:33:46 | Add custom bootstrap ldif...
openldap  | ***  INFO   | 2024-02-12 11:33:46 | Add TLS config...
openldap  | ***  INFO   | 2024-02-12 11:33:46 | No certificate file and certificate key provided, generate:
openldap  | ***  INFO   | 2024-02-12 11:33:46 | /container/service/slapd/assets/certs/ldap.crt and /container/service/slapd/assets/certs/ldap.key
openldap  | 2024/02/12 11:33:47 [INFO] generate received request
openldap  | 2024/02/12 11:33:47 [INFO] received CSR
openldap  | 2024/02/12 11:33:47 [INFO] generating key: ecdsa-384
openldap  | 2024/02/12 11:33:47 [INFO] encoded CSR
openldap  | 2024/02/12 11:33:47 [INFO] signed certificate with serial number 63303743974716622619596598691848524209955130579
openldap  | ***  INFO   | 2024-02-12 11:33:47 | Link /container/service/:ssl-tools/assets/default-ca/default-ca.pem to /container/service/slapd/assets/certs/ca.crt
openldap  | ***  INFO   | 2024-02-12 11:33:47 | Disable replication config...
openldap  | ***  INFO   | 2024-02-12 11:33:47 | Stop OpenLDAP...
openldap  | ***  INFO   | 2024-02-12 11:33:47 | Configure ldap client TLS configuration...
openldap  | ***  INFO   | 2024-02-12 11:33:47 | Remove config files...
openldap  | ***  INFO   | 2024-02-12 11:33:47 | First start is done...
openldap  | ***  INFO   | 2024-02-12 11:33:47 | Remove file /container/environment/99-default/default.startup.yaml
openldap  | ***  INFO   | 2024-02-12 11:33:47 | Environment files will be proccessed in this order : 
openldap  | Caution: previously defined variables will not be overriden.
openldap  | /container/environment/99-default/default.yaml
openldap  | 
openldap  | To see how this files are processed and environment variables values,
openldap  | run this container with '--loglevel debug'
openldap  | ***  INFO   | 2024-02-12 11:33:47 | Running /container/run/process/slapd/run...
openldap  | 65ca021b @(#) $OpenLDAP: slapd 2.4.57+dfsg-1~bpo10+1 (Jan 30 2021 06:59:51) $
openldap  | 	Debian OpenLDAP Maintainers <pkg-openldap-devel@lists.alioth.debian.org>
openldap  | 65ca021b slapd starting
openldap  | 65ca023d conn=1000 fd=12 ACCEPT from IP=172.20.0.2:35446 (IP=0.0.0.0:389)
openldap  | 65ca023d conn=1000 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap  | 65ca023d conn=1000 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui   | [2024-02-12 11:34:21 +0000] [8] [INFO] 172.20.0.1:49248 - - [12/Feb/2024:11:34:21 +0000] "GET /api/whoami 1.1" 500 127 "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:34:21 +0000] [8] [INFO] 172.20.0.1:49248 - - [12/Feb/2024:11:34:21 +0000] "GET /api/whoami 1.1" - - "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
openldap  | 65ca023d conn=1001 fd=13 ACCEPT from IP=172.20.0.2:35458 (IP=0.0.0.0:389)
openldap  | 65ca023d conn=1001 op=0 SRCH base="dc=ldap,dc=server,dc=rlik" scope=2 deref=0 filter="(uid=admin)"
openldap  | 65ca023d conn=1001 op=0 SEARCH RESULT tag=101 err=32 nentries=0 text=
ldap_ui   | [2024-02-12 11:34:21 +0000] [8] [INFO] 172.20.0.1:49248 - - [12/Feb/2024:11:34:21 +0000] "GET /api/schema 1.1" 500 127 "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
ldap_ui   | [2024-02-12 11:34:21 +0000] [8] [INFO] 172.20.0.1:49248 - - [12/Feb/2024:11:34:21 +0000] "GET /api/schema 1.1" - - "http://127.0.0.1:5000/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
