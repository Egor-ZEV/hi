phpldapadmin-1  | *** CONTAINER_LOG_LEVEL = 3 (info)
phpldapadmin-1  | *** Search service in CONTAINER_SERVICE_DIR = /container/service :
phpldapadmin-1  | *** link /container/service/:apache2/startup.sh to /container/run/startup/:apache2
phpldapadmin-1  | *** link /container/service/:apache2/process.sh to /container/run/process/:apache2/run
phpldapadmin-1  | *** link /container/service/:apache2/finish.sh to /container/run/process/:apache2/finish
phpldapadmin-1  | *** link /container/service/:cron/startup.sh to /container/run/startup/:cron
phpldapadmin-1  | *** link /container/service/:cron/process.sh to /container/run/process/:cron/run
phpldapadmin-1  | *** link /container/service/:logrotate/startup.sh to /container/run/startup/:logrotate
phpldapadmin-1  | *** link /container/service/:php7.3-fpm/startup.sh to /container/run/startup/:php7.3-fpm
phpldapadmin-1  | *** link /container/service/:php7.3-fpm/process.sh to /container/run/process/:php7.3-fpm/run
phpldapadmin-1  | *** link /container/service/:ssl-tools/startup.sh to /container/run/startup/:ssl-tools
phpldapadmin-1  | *** link /container/service/:syslog-ng-core/startup.sh to /container/run/startup/:syslog-ng-core
phpldapadmin-1  | *** link /container/service/:syslog-ng-core/process.sh to /container/run/process/:syslog-ng-core/run
phpldapadmin-1  | *** link /container/service/ldap-client/startup.sh to /container/run/startup/ldap-client
phpldapadmin-1  | *** link /container/service/phpldapadmin/startup.sh to /container/run/startup/phpldapadmin
phpldapadmin-1  | *** Set environment for startup files
phpldapadmin-1  | *** Environment files will be proccessed in this order : 
phpldapadmin-1  | Caution: previously defined variables will not be overriden.
phpldapadmin-1  | /container/environment/99-default/default.yaml
phpldapadmin-1  | /container/environment/99-default/default.startup.yaml
phpldapadmin-1  | 
phpldapadmin-1  | To see how this files are processed and environment variables values,
phpldapadmin-1  | run this container with '--loglevel debug'
phpldapadmin-1  | *** Running /container/run/startup/:apache2...
phpldapadmin-1  | *** Running /container/run/startup/:cron...
phpldapadmin-1  | *** Running /container/run/startup/:logrotate...
phpldapadmin-1  | *** Running /container/run/startup/:php7.3-fpm...
openldap-1      | ***  INFO   | 2024-02-12 10:43:34 | CONTAINER_LOG_LEVEL = 3 (info)
openldap-1      | ***  INFO   | 2024-02-12 10:43:34 | Search service in CONTAINER_SERVICE_DIR = /container/service :
openldap-1      | ***  INFO   | 2024-02-12 10:43:34 | link /container/service/:ssl-tools/startup.sh to /container/run/startup/:ssl-tools
openldap-1      | ***  INFO   | 2024-02-12 10:43:34 | link /container/service/slapd/startup.sh to /container/run/startup/slapd
openldap-1      | ***  INFO   | 2024-02-12 10:43:34 | link /container/service/slapd/process.sh to /container/run/process/slapd/run
openldap-1      | ***  INFO   | 2024-02-12 10:43:35 | Environment files will be proccessed in this order : 
openldap-1      | Caution: previously defined variables will not be overriden.
openldap-1      | /container/environment/99-default/default.yaml
openldap-1      | /container/environment/99-default/default.startup.yaml
openldap-1      | 
openldap-1      | To see how this files are processed and environment variables values,
openldap-1      | run this container with '--loglevel debug'
openldap-1      | ***  INFO   | 2024-02-12 10:43:35 | Running /container/run/startup/:ssl-tools...
phpldapadmin-1  | *** Running /container/run/startup/:ssl-tools...
phpldapadmin-1  | *** Running /container/run/startup/:syslog-ng-core...
phpldapadmin-1  | *** Running /container/run/startup/ldap-client...
openldap-1      | ***  INFO   | 2024-02-12 10:43:35 | Running /container/run/startup/slapd...
phpldapadmin-1  | No certificate file and certificate key provided, generate:
phpldapadmin-1  | /container/service/ldap-client/assets/certs/ldap-client.crt and /container/service/ldap-client/assets/certs/ldap-client.key
openldap-1      | ***  INFO   | 2024-02-12 10:43:35 | openldap user and group adjustments
openldap-1      | ***  INFO   | 2024-02-12 10:43:35 | get current openldap uid/gid info inside container
openldap-1      | ***  INFO   | 2024-02-12 10:43:35 | -------------------------------------
openldap-1      | ***  INFO   | 2024-02-12 10:43:35 | openldap GID/UID
openldap-1      | ***  INFO   | 2024-02-12 10:43:35 | -------------------------------------
openldap-1      | ***  INFO   | 2024-02-12 10:43:35 | User uid: 911
openldap-1      | ***  INFO   | 2024-02-12 10:43:35 | User gid: 911
openldap-1      | ***  INFO   | 2024-02-12 10:43:35 | uid/gid changed: false
openldap-1      | ***  INFO   | 2024-02-12 10:43:36 | -------------------------------------
phpldapadmin-1  | 2024/02/12 10:43:36 [INFO] generate received request
phpldapadmin-1  | 2024/02/12 10:43:36 [INFO] received CSR
phpldapadmin-1  | 2024/02/12 10:43:36 [INFO] generating key: ecdsa-384
openldap-1      | ***  INFO   | 2024-02-12 10:43:36 | updating file uid/gid ownership
phpldapadmin-1  | 2024/02/12 10:43:36 [INFO] encoded CSR
phpldapadmin-1  | 2024/02/12 10:43:36 [INFO] signed certificate with serial number 561070676906801179602486039063721209420663092591
phpldapadmin-1  | Link /container/service/:ssl-tools/assets/default-ca/default-ca.pem to /container/service/ldap-client/assets/certs/ldap-ca.crt
phpldapadmin-1  | *** Running /container/run/startup/phpldapadmin...
phpldapadmin-1  | Set apache2 http config...
phpldapadmin-1  | Bootstap phpLDAPadmin...
phpldapadmin-1  | tr: write error: Broken pipe
phpldapadmin-1  | tr: write error
phpldapadmin-1  | *** Set environment for container process
phpldapadmin-1  | *** Remove file /container/environment/99-default/default.startup.yaml
phpldapadmin-1  | *** Environment files will be proccessed in this order : 
phpldapadmin-1  | Caution: previously defined variables will not be overriden.
phpldapadmin-1  | /container/environment/99-default/default.yaml
phpldapadmin-1  | 
phpldapadmin-1  | To see how this files are processed and environment variables values,
phpldapadmin-1  | run this container with '--loglevel debug'
phpldapadmin-1  | *** Running runit daemon...
phpldapadmin-1  | Feb 12 10:43:39 6d52f0d0e0fa syslog-ng[858]: syslog-ng starting up; version='3.19.1'
phpldapadmin-1  | [12-Feb-2024 10:43:39] NOTICE: fpm is running, pid 856
phpldapadmin-1  | [12-Feb-2024 10:43:39] NOTICE: ready to handle connections
phpldapadmin-1  | [12-Feb-2024 10:43:39] NOTICE: systemd monitor interval set to 10000ms
openldap-1      | ***  INFO   | 2024-02-12 10:43:39 | Database and config directory are empty...
phpldapadmin-1  | AH00558: apache2: Could not reliably determine the server's fully qualified domain name, using 172.19.0.3. Set the 'ServerName' directive globally to suppress this message
phpldapadmin-1  | [Mon Feb 12 10:43:39.469567 2024] [ssl:warn] [pid 869:tid 139937286648960] AH01882: Init: this version of mod_ssl was compiled against a newer library (OpenSSL 1.1.1d  10 Sep 2019, version currently loaded is OpenSSL 1.1.1c  28 May 2019) - may result in undefined or erroneous behavior
openldap-1      | ***  INFO   | 2024-02-12 10:43:39 | Init new ldap server...
phpldapadmin-1  | AH00558: apache2: Could not reliably determine the server's fully qualified domain name, using 172.19.0.3. Set the 'ServerName' directive globally to suppress this message
phpldapadmin-1  | [Mon Feb 12 10:43:39.509844 2024] [ssl:warn] [pid 869:tid 139937286648960] AH01882: Init: this version of mod_ssl was compiled against a newer library (OpenSSL 1.1.1d  10 Sep 2019, version currently loaded is OpenSSL 1.1.1c  28 May 2019) - may result in undefined or erroneous behavior
phpldapadmin-1  | [Mon Feb 12 10:43:39.521676 2024] [mpm_event:notice] [pid 869:tid 139937286648960] AH00489: Apache/2.4.38 (Debian) OpenSSL/1.1.1c configured -- resuming normal operations
phpldapadmin-1  | [Mon Feb 12 10:43:39.522490 2024] [core:notice] [pid 869:tid 139937286648960] AH00094: Command line: '/usr/sbin/apache2 -D FOREGROUND'
openldap-1      |   Backing up /etc/ldap/slapd.d in /var/backups/slapd-2.4.57+dfsg-1~bpo10+1... done.
openldap-1      |   Creating initial configuration... done.
openldap-1      |   Creating LDAP directory... done.
openldap-1      | invoke-rc.d: could not determine current runlevel
openldap-1      | invoke-rc.d: policy-rc.d denied execution of restart.
openldap-1      | ***  INFO   | 2024-02-12 10:43:41 | Start OpenLDAP...
openldap-1      | ***  INFO   | 2024-02-12 10:43:42 | Waiting for OpenLDAP to start...
openldap-1      | ***  INFO   | 2024-02-12 10:43:42 | Add bootstrap schemas...
openldap-1      | config file testing succeeded
openldap-1      | ***  INFO   | 2024-02-12 10:43:43 | Add image bootstrap ldif...
openldap-1      | ***  INFO   | 2024-02-12 10:43:43 | Add custom bootstrap ldif...
openldap-1      | ***  INFO   | 2024-02-12 10:43:43 | Add TLS config...
openldap-1      | ***  INFO   | 2024-02-12 10:43:43 | No certificate file and certificate key provided, generate:
openldap-1      | ***  INFO   | 2024-02-12 10:43:43 | /container/service/slapd/assets/certs/ldap.crt and /container/service/slapd/assets/certs/ldap.key
openldap-1      | 2024/02/12 10:43:43 [INFO] generate received request
openldap-1      | 2024/02/12 10:43:43 [INFO] received CSR
openldap-1      | 2024/02/12 10:43:43 [INFO] generating key: ecdsa-384
openldap-1      | 2024/02/12 10:43:43 [INFO] encoded CSR
openldap-1      | 2024/02/12 10:43:44 [INFO] signed certificate with serial number 167471368166014498995561150143151688196857357901
openldap-1      | ***  INFO   | 2024-02-12 10:43:44 | Link /container/service/:ssl-tools/assets/default-ca/default-ca.pem to /container/service/slapd/assets/certs/ca.crt
openldap-1      | ***  INFO   | 2024-02-12 10:43:44 | Disable replication config...
openldap-1      | ***  INFO   | 2024-02-12 10:43:44 | Stop OpenLDAP...
openldap-1      | ***  INFO   | 2024-02-12 10:43:44 | Configure ldap client TLS configuration...
openldap-1      | ***  INFO   | 2024-02-12 10:43:44 | Remove config files...
openldap-1      | ***  INFO   | 2024-02-12 10:43:44 | First start is done...
openldap-1      | ***  INFO   | 2024-02-12 10:43:44 | Remove file /container/environment/99-default/default.startup.yaml
openldap-1      | ***  INFO   | 2024-02-12 10:43:44 | Environment files will be proccessed in this order : 
openldap-1      | Caution: previously defined variables will not be overriden.
openldap-1      | /container/environment/99-default/default.yaml
openldap-1      | 
openldap-1      | To see how this files are processed and environment variables values,
openldap-1      | run this container with '--loglevel debug'
openldap-1      | ***  INFO   | 2024-02-12 10:43:44 | Running /container/run/process/slapd/run...
openldap-1      | 65c9f660 @(#) $OpenLDAP: slapd 2.4.57+dfsg-1~bpo10+1 (Jan 30 2021 06:59:51) $
openldap-1      | 	Debian OpenLDAP Maintainers <pkg-openldap-devel@lists.alioth.debian.org>
openldap-1      | 65c9f660 slapd starting
