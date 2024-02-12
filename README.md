docker logs dockers-phpldapadmin-1
*** CONTAINER_LOG_LEVEL = 3 (info)
*** Search service in CONTAINER_SERVICE_DIR = /container/service :
*** link /container/service/:apache2/startup.sh to /container/run/startup/:apache2
*** link /container/service/:apache2/process.sh to /container/run/process/:apache2/run
*** link /container/service/:apache2/finish.sh to /container/run/process/:apache2/finish
*** link /container/service/:cron/startup.sh to /container/run/startup/:cron
*** link /container/service/:cron/process.sh to /container/run/process/:cron/run
*** link /container/service/:logrotate/startup.sh to /container/run/startup/:logrotate
*** link /container/service/:php7.3-fpm/startup.sh to /container/run/startup/:php7.3-fpm
*** link /container/service/:php7.3-fpm/process.sh to /container/run/process/:php7.3-fpm/run
*** link /container/service/:ssl-tools/startup.sh to /container/run/startup/:ssl-tools
*** link /container/service/:syslog-ng-core/startup.sh to /container/run/startup/:syslog-ng-core
*** link /container/service/:syslog-ng-core/process.sh to /container/run/process/:syslog-ng-core/run
*** link /container/service/ldap-client/startup.sh to /container/run/startup/ldap-client
*** link /container/service/phpldapadmin/startup.sh to /container/run/startup/phpldapadmin
*** Set environment for startup files
*** Environment files will be proccessed in this order : 
Caution: previously defined variables will not be overriden.
/container/environment/99-default/default.yaml
/container/environment/99-default/default.startup.yaml

To see how this files are processed and environment variables values,
run this container with '--loglevel debug'
*** Running /container/run/startup/:apache2...
*** Running /container/run/startup/:cron...
*** Running /container/run/startup/:logrotate...
*** Running /container/run/startup/:php7.3-fpm...
*** Running /container/run/startup/:ssl-tools...
*** Running /container/run/startup/:syslog-ng-core...
*** Running /container/run/startup/ldap-client...
No certificate file and certificate key provided, generate:
/container/service/ldap-client/assets/certs/ldap-client.crt and /container/service/ldap-client/assets/certs/ldap-client.key
2024/02/12 10:13:45 [INFO] generate received request
2024/02/12 10:13:45 [INFO] received CSR
2024/02/12 10:13:45 [INFO] generating key: ecdsa-384
2024/02/12 10:13:46 [INFO] encoded CSR
2024/02/12 10:13:46 [INFO] signed certificate with serial number 547044447389909999988292269751346142141952651734
Link /container/service/:ssl-tools/assets/default-ca/default-ca.pem to /container/service/ldap-client/assets/certs/ldap-ca.crt
*** Running /container/run/startup/phpldapadmin...
Set apache2 http config...
*** Set environment for container process
*** Remove file /container/environment/99-default/default.startup.yaml
*** Environment files will be proccessed in this order : 
Caution: previously defined variables will not be overriden.
/container/environment/99-default/default.yaml

To see how this files are processed and environment variables values,
run this container with '--loglevel debug'
*** Running runit daemon...
AH00558: apache2: Could not reliably determine the server's fully qualified domain name, using 172.28.0.3. Set the 'ServerName' directive globally to suppress this message
[Mon Feb 12 10:14:42.684037 2024] [ssl:warn] [pid 1520:tid 140013723726976] AH01882: Init: this version of mod_ssl was compiled against a newer library (OpenSSL 1.1.1d  10 Sep 2019, version currently loaded is OpenSSL 1.1.1c  28 May 2019) - may result in undefined or erroneous behavior
AH00558: apache2: Could not reliably determine the server's fully qualified domain name, using 172.28.0.3. Set the 'ServerName' directive globally to suppress this message
[Mon Feb 12 10:14:42.722647 2024] [ssl:warn] [pid 1520:tid 140013723726976] AH01882: Init: this version of mod_ssl was compiled against a newer library (OpenSSL 1.1.1d  10 Sep 2019, version currently loaded is OpenSSL 1.1.1c  28 May 2019) - may result in undefined or erroneous behavior
[Mon Feb 12 10:14:42.729581 2024] [mpm_event:notice] [pid 1520:tid 140013723726976] AH00489: Apache/2.4.38 (Debian) OpenSSL/1.1.1c configured -- resuming normal operations
[Mon Feb 12 10:14:42.729796 2024] [core:notice] [pid 1520:tid 140013723726976] AH00094: Command line: '/usr/sbin/apache2 -D FOREGROUND'
Feb 12 10:14:42 0a42373798ca syslog-ng[1505]: syslog-ng starting up; version='3.19.1'
[12-Feb-2024 10:14:43] NOTICE: fpm is running, pid 1506
[12-Feb-2024 10:14:43] NOTICE: ready to handle connections
[12-Feb-2024 10:14:43] NOTICE: systemd monitor interval set to 10000ms
172.28.0.1 - - [12/Feb/2024:10:14:56 +0000] "GET / HTTP/1.1" 200 1854 "-" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
172.28.0.1 - - [12/Feb/2024:10:15:04 +0000] "GET /cmd.php?cmd=login_form&server_id=1&meth=ajax HTTP/1.1" 200 1074 "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
Feb 12 10:17:01 0a42373798ca CRON[1657]: (root) CMD (   cd / && run-parts --report /etc/cron.hourly)
172.28.0.1 - - [12/Feb/2024:10:19:27 +0000] "POST /cmd.php HTTP/1.1" 302 473 "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
172.28.0.1 - - [12/Feb/2024:10:19:27 +0000] "GET /cmd.php?cmd=login_form&server_id=1&redirect=true HTTP/1.1" 200 2303 "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
172.28.0.1 - - [12/Feb/2024:10:20:15 +0000] "GET /cmd.php?cmd=login_form&server_id=1&redirect=true HTTP/1.1" 200 2207 "http://127.0.0.1:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
172.28.0.1 - - [12/Feb/2024:10:20:27 +0000] "POST /cmd.php HTTP/1.1" 302 473 "http://127.0.0.1:8080/cmd.php?cmd=login_form&server_id=1&redirect=true" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
172.28.0.1 - - [12/Feb/2024:10:20:27 +0000] "GET /cmd.php?cmd=login_form&server_id=1&redirect=true HTTP/1.1" 200 2303 "http://127.0.0.1:8080/cmd.php?cmd=login_form&server_id=1&redirect=true" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 YaBrowser/23.11.0.0 Safari/537.36"
