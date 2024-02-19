root@cf649877b739:/# freeradius -X
FreeRADIUS Version 3.2.3
Copyright (C) 1999-2022 The FreeRADIUS server project and contributors
There is NO warranty; not even for MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE
You may redistribute copies of FreeRADIUS under the terms of the
GNU General Public License
For more information about these matters, see the file named COPYRIGHT
Starting - reading configuration files ...
including dictionary file /usr/share/freeradius/dictionary
including dictionary file /usr/share/freeradius/dictionary.dhcp
including dictionary file /usr/share/freeradius/dictionary.vqp
including dictionary file /etc/freeradius/dictionary
including configuration file /etc/freeradius/radiusd.conf
including configuration file /etc/freeradius/proxy.conf
including configuration file /etc/freeradius/clients.conf
including files in directory /etc/freeradius/mods-enabled/
including configuration file /etc/freeradius/mods-enabled/realm
including configuration file /etc/freeradius/mods-enabled/detail
including configuration file /etc/freeradius/mods-enabled/linelog
including configuration file /etc/freeradius/mods-enabled/replicate
including configuration file /etc/freeradius/mods-enabled/echo
including configuration file /etc/freeradius/mods-enabled/detail.log
including configuration file /etc/freeradius/mods-enabled/sradutmp
including configuration file /etc/freeradius/mods-enabled/unix
including configuration file /etc/freeradius/mods-enabled/always
including configuration file /etc/freeradius/mods-enabled/totp
including configuration file /etc/freeradius/mods-enabled/digest
including configuration file /etc/freeradius/mods-enabled/preprocess
including configuration file /etc/freeradius/mods-enabled/attr_filter
including configuration file /etc/freeradius/mods-enabled/chap
including configuration file /etc/freeradius/mods-enabled/logintime
including configuration file /etc/freeradius/mods-enabled/dynamic_clients
including configuration file /etc/freeradius/mods-enabled/soh
including configuration file /etc/freeradius/mods-enabled/mschap
including configuration file /etc/freeradius/mods-enabled/ntlm_auth
including configuration file /etc/freeradius/mods-enabled/radutmp
including configuration file /etc/freeradius/mods-enabled/expr
including configuration file /etc/freeradius/mods-enabled/passwd
including configuration file /etc/freeradius/mods-enabled/exec
including configuration file /etc/freeradius/mods-enabled/date
including configuration file /etc/freeradius/mods-enabled/files
including configuration file /etc/freeradius/mods-enabled/unpack
including configuration file /etc/freeradius/mods-enabled/expiration
including configuration file /etc/freeradius/mods-enabled/utf8
including configuration file /etc/freeradius/mods-enabled/pap
including configuration file /etc/freeradius/mods-enabled/ldap
including files in directory /etc/freeradius/policy.d/
including configuration file /etc/freeradius/policy.d/eap
including configuration file /etc/freeradius/policy.d/canonicalization
including configuration file /etc/freeradius/policy.d/abfab-tr
including configuration file /etc/freeradius/policy.d/control
including configuration file /etc/freeradius/policy.d/moonshot-targeted-ids
including configuration file /etc/freeradius/policy.d/dhcp
including configuration file /etc/freeradius/policy.d/rfc7542
including configuration file /etc/freeradius/policy.d/debug
including configuration file /etc/freeradius/policy.d/operator-name
including configuration file /etc/freeradius/policy.d/accounting
including configuration file /etc/freeradius/policy.d/filter
including configuration file /etc/freeradius/policy.d/cui
including files in directory /etc/freeradius/sites-enabled/
including configuration file /etc/freeradius/sites-enabled/my_server
main {
 security {
 	user = "freerad"
 	group = "freerad"
 	allow_core_dumps = no
 }
	name = "freeradius"
	prefix = "/usr"
	localstatedir = "/var"
	logdir = "/var/log/freeradius"
	run_dir = "/var/run/freeradius"
}
main {
	name = "freeradius"
	prefix = "/usr"
	localstatedir = "/var"
	sbindir = "/usr/sbin"
	logdir = "/var/log/freeradius"
	run_dir = "/var/run/freeradius"
	libdir = "/usr/lib/freeradius"
	radacctdir = "/var/log/freeradius/radacct"
	hostname_lookups = no
	max_request_time = 30
	cleanup_delay = 5
	max_requests = 16384
	postauth_client_lost = no
	pidfile = "/var/run/freeradius/freeradius.pid"
	checkrad = "/usr/sbin/checkrad"
	debug_level = 0
	proxy_requests = yes
 log {
 	stripped_names = no
 	auth = no
 	auth_badpass = no
 	auth_goodpass = no
 	colourise = yes
 	msg_denied = "You are already logged in - access denied"
 }
 resources {
 }
 security {
 	max_attributes = 200
 	reject_delay = 1.000000
 	status_server = yes
 }
}
radiusd: #### Loading Realms and Home Servers ####
 proxy server {
 	retry_delay = 5
 	retry_count = 3
 	default_fallback = no
 	dead_time = 120
 	wake_all_if_all_dead = no
 }
 home_server localhost {
 	nonblock = no
 	ipaddr = 127.0.0.1
 	port = 1812
 	type = "auth"
 	secret = <<< secret >>>
 	response_window = 20.000000
 	response_timeouts = 1
 	max_outstanding = 65536
 	zombie_period = 40
 	status_check = "status-server"
 	ping_interval = 30
 	check_interval = 30
 	check_timeout = 4
 	num_answers_to_alive = 3
 	revive_interval = 120
  limit {
  	max_connections = 16
  	max_requests = 0
  	lifetime = 0
  	idle_timeout = 0
  }
  coa {
  	irt = 2
  	mrt = 16
  	mrc = 5
  	mrd = 30
  }
  recv_coa {
  }
 }
 home_server_pool my_auth_failover {
	type = fail-over
	home_server = localhost
 }
 realm example.com {
	auth_pool = my_auth_failover
 }
 realm LOCAL {
 }
radiusd: #### Loading Clients ####
 client localhost {
 	ipaddr = 127.0.0.1
 	require_message_authenticator = no
 	secret = <<< secret >>>
 	nas_type = "other"
 	proto = "*"
  limit {
  	max_connections = 16
  	lifetime = 0
  	idle_timeout = 30
  }
 }
 client localhost_ipv6 {
 	ipv6addr = ::1
 	require_message_authenticator = no
 	secret = <<< secret >>>
  limit {
  	max_connections = 16
  	lifetime = 0
  	idle_timeout = 30
  }
 }
Debug state unknown (cap_sys_ptrace capability not set)
systemd watchdog is disabled
 # Creating Auth-Type = LDAP
radiusd: #### Instantiating modules ####
 modules {
  # Loaded module rlm_realm
  # Loading module "IPASS" from file /etc/freeradius/mods-enabled/realm
  realm IPASS {
  	format = "prefix"
  	delimiter = "/"
  	ignore_default = no
  	ignore_null = no
  }
  # Loading module "suffix" from file /etc/freeradius/mods-enabled/realm
  realm suffix {
  	format = "suffix"
  	delimiter = "@"
  	ignore_default = no
  	ignore_null = no
  }
  # Loading module "bangpath" from file /etc/freeradius/mods-enabled/realm
  realm bangpath {
  	format = "prefix"
  	delimiter = "!"
  	ignore_default = no
  	ignore_null = no
  }
  # Loading module "realmpercent" from file /etc/freeradius/mods-enabled/realm
  realm realmpercent {
  	format = "suffix"
  	delimiter = "%"
  	ignore_default = no
  	ignore_null = no
  }
  # Loading module "ntdomain" from file /etc/freeradius/mods-enabled/realm
  realm ntdomain {
  	format = "prefix"
  	delimiter = "\\"
  	ignore_default = no
  	ignore_null = no
  }
  # Loaded module rlm_detail
  # Loading module "detail" from file /etc/freeradius/mods-enabled/detail
  detail {
  	filename = "/var/log/freeradius/radacct/%{%{Packet-Src-IP-Address}:-%{Packet-Src-IPv6-Address}}/detail-%Y%m%d"
  	header = "%t"
  	permissions = 384
  	locking = no
  	escape_filenames = no
  	log_packet_header = no
  }
  # Loaded module rlm_linelog
  # Loading module "linelog" from file /etc/freeradius/mods-enabled/linelog
  linelog {
  	filename = "/var/log/freeradius/linelog"
  	escape_filenames = no
  	syslog_severity = "info"
  	permissions = 384
  	format = "This is a log message for %{User-Name}"
  	reference = "messages.%{%{reply:Packet-Type}:-default}"
  }
  # Loading module "log_accounting" from file /etc/freeradius/mods-enabled/linelog
  linelog log_accounting {
  	filename = "/var/log/freeradius/linelog-accounting"
  	escape_filenames = no
  	syslog_severity = "info"
  	permissions = 384
  	format = ""
  	reference = "Accounting-Request.%{%{Acct-Status-Type}:-unknown}"
  }
  # Loaded module rlm_replicate
  # Loading module "replicate" from file /etc/freeradius/mods-enabled/replicate
  # Loaded module rlm_exec
  # Loading module "echo" from file /etc/freeradius/mods-enabled/echo
  exec echo {
  	wait = yes
  	program = "/bin/echo %{User-Name}"
  	input_pairs = "request"
  	output_pairs = "reply"
  	shell_escape = yes
  }
  # Loading module "auth_log" from file /etc/freeradius/mods-enabled/detail.log
  detail auth_log {
  	filename = "/var/log/freeradius/radacct/%{%{Packet-Src-IP-Address}:-%{Packet-Src-IPv6-Address}}/auth-detail-%Y%m%d"
  	header = "%t"
  	permissions = 384
  	locking = no
  	escape_filenames = no
  	log_packet_header = no
  }
  # Loading module "reply_log" from file /etc/freeradius/mods-enabled/detail.log
  detail reply_log {
  	filename = "/var/log/freeradius/radacct/%{%{Packet-Src-IP-Address}:-%{Packet-Src-IPv6-Address}}/reply-detail-%Y%m%d"
  	header = "%t"
  	permissions = 384
  	locking = no
  	escape_filenames = no
  	log_packet_header = no
  }
  # Loading module "pre_proxy_log" from file /etc/freeradius/mods-enabled/detail.log
  detail pre_proxy_log {
  	filename = "/var/log/freeradius/radacct/%{%{Packet-Src-IP-Address}:-%{Packet-Src-IPv6-Address}}/pre-proxy-detail-%Y%m%d"
  	header = "%t"
  	permissions = 384
  	locking = no
  	escape_filenames = no
  	log_packet_header = no
  }
  # Loading module "post_proxy_log" from file /etc/freeradius/mods-enabled/detail.log
  detail post_proxy_log {
  	filename = "/var/log/freeradius/radacct/%{%{Packet-Src-IP-Address}:-%{Packet-Src-IPv6-Address}}/post-proxy-detail-%Y%m%d"
  	header = "%t"
  	permissions = 384
  	locking = no
  	escape_filenames = no
  	log_packet_header = no
  }
  # Loaded module rlm_radutmp
  # Loading module "sradutmp" from file /etc/freeradius/mods-enabled/sradutmp
  radutmp sradutmp {
  	filename = "/var/log/freeradius/sradutmp"
  	username = "%{User-Name}"
  	case_sensitive = yes
  	check_with_nas = yes
  	permissions = 420
  	caller_id = no
  }
  # Loaded module rlm_unix
  # Loading module "unix" from file /etc/freeradius/mods-enabled/unix
  unix {
  	radwtmp = "/var/log/freeradius/radwtmp"
  }
Creating attribute Unix-Group
  # Loaded module rlm_always
  # Loading module "reject" from file /etc/freeradius/mods-enabled/always
  always reject {
  	rcode = "reject"
  	simulcount = 0
  	mpp = no
  }
  # Loading module "fail" from file /etc/freeradius/mods-enabled/always
  always fail {
  	rcode = "fail"
  	simulcount = 0
  	mpp = no
  }
  # Loading module "ok" from file /etc/freeradius/mods-enabled/always
  always ok {
  	rcode = "ok"
  	simulcount = 0
  	mpp = no
  }
  # Loading module "handled" from file /etc/freeradius/mods-enabled/always
  always handled {
  	rcode = "handled"
  	simulcount = 0
  	mpp = no
  }
  # Loading module "invalid" from file /etc/freeradius/mods-enabled/always
  always invalid {
  	rcode = "invalid"
  	simulcount = 0
  	mpp = no
  }
  # Loading module "userlock" from file /etc/freeradius/mods-enabled/always
  always userlock {
  	rcode = "userlock"
  	simulcount = 0
  	mpp = no
  }
  # Loading module "notfound" from file /etc/freeradius/mods-enabled/always
  always notfound {
  	rcode = "notfound"
  	simulcount = 0
  	mpp = no
  }
  # Loading module "noop" from file /etc/freeradius/mods-enabled/always
  always noop {
  	rcode = "noop"
  	simulcount = 0
  	mpp = no
  }
  # Loading module "updated" from file /etc/freeradius/mods-enabled/always
  always updated {
  	rcode = "updated"
  	simulcount = 0
  	mpp = no
  }
  # Loaded module rlm_totp
  # Loading module "totp" from file /etc/freeradius/mods-enabled/totp
  # Loaded module rlm_digest
  # Loading module "digest" from file /etc/freeradius/mods-enabled/digest
  # Loaded module rlm_preprocess
  # Loading module "preprocess" from file /etc/freeradius/mods-enabled/preprocess
  preprocess {
  	huntgroups = "/etc/freeradius/mods-config/preprocess/huntgroups"
  	hints = "/etc/freeradius/mods-config/preprocess/hints"
  	with_ascend_hack = no
  	ascend_channels_per_line = 23
  	with_ntdomain_hack = no
  	with_specialix_jetstream_hack = no
  	with_cisco_vsa_hack = no
  	with_alvarion_vsa_hack = no
  }
  # Loaded module rlm_attr_filter
  # Loading module "attr_filter.post-proxy" from file /etc/freeradius/mods-enabled/attr_filter
  attr_filter attr_filter.post-proxy {
  	filename = "/etc/freeradius/mods-config/attr_filter/post-proxy"
  	key = "%{Realm}"
  	relaxed = no
  }
  # Loading module "attr_filter.pre-proxy" from file /etc/freeradius/mods-enabled/attr_filter
  attr_filter attr_filter.pre-proxy {
  	filename = "/etc/freeradius/mods-config/attr_filter/pre-proxy"
  	key = "%{Realm}"
  	relaxed = no
  }
  # Loading module "attr_filter.access_reject" from file /etc/freeradius/mods-enabled/attr_filter
  attr_filter attr_filter.access_reject {
  	filename = "/etc/freeradius/mods-config/attr_filter/access_reject"
  	key = "%{User-Name}"
  	relaxed = no
  }
  # Loading module "attr_filter.access_challenge" from file /etc/freeradius/mods-enabled/attr_filter
  attr_filter attr_filter.access_challenge {
  	filename = "/etc/freeradius/mods-config/attr_filter/access_challenge"
  	key = "%{User-Name}"
  	relaxed = no
  }
  # Loading module "attr_filter.accounting_response" from file /etc/freeradius/mods-enabled/attr_filter
  attr_filter attr_filter.accounting_response {
  	filename = "/etc/freeradius/mods-config/attr_filter/accounting_response"
  	key = "%{User-Name}"
  	relaxed = no
  }
  # Loading module "attr_filter.coa" from file /etc/freeradius/mods-enabled/attr_filter
  attr_filter attr_filter.coa {
  	filename = "/etc/freeradius/mods-config/attr_filter/coa"
  	key = "%{User-Name}"
  	relaxed = no
  }
  # Loaded module rlm_chap
  # Loading module "chap" from file /etc/freeradius/mods-enabled/chap
  # Loaded module rlm_logintime
  # Loading module "logintime" from file /etc/freeradius/mods-enabled/logintime
  logintime {
  	minimum_timeout = 60
  }
  # Loaded module rlm_dynamic_clients
  # Loading module "dynamic_clients" from file /etc/freeradius/mods-enabled/dynamic_clients
  # Loaded module rlm_soh
  # Loading module "soh" from file /etc/freeradius/mods-enabled/soh
  soh {
  	dhcp = yes
  }
  # Loaded module rlm_mschap
  # Loading module "mschap" from file /etc/freeradius/mods-enabled/mschap
  mschap {
  	use_mppe = yes
  	require_encryption = no
  	require_strong = no
  	with_ntdomain_hack = yes
   passchange {
   }
  	allow_retry = yes
  	winbind_retry_with_normalised_username = no
  }
  # Loading module "ntlm_auth" from file /etc/freeradius/mods-enabled/ntlm_auth
  exec ntlm_auth {
  	wait = yes
  	program = "/path/to/ntlm_auth --request-nt-key --domain=MYDOMAIN --username=%{mschap:User-Name} --password=%{User-Password}"
  	shell_escape = yes
  }
  # Loading module "radutmp" from file /etc/freeradius/mods-enabled/radutmp
  radutmp {
  	filename = "/var/log/freeradius/radutmp"
  	username = "%{User-Name}"
  	case_sensitive = yes
  	check_with_nas = yes
  	permissions = 384
  	caller_id = yes
  }
  # Loaded module rlm_expr
  # Loading module "expr" from file /etc/freeradius/mods-enabled/expr
  expr {
  	safe_characters = "@abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789.-_: /äéöüàâæçèéêëîïôœùûüaÿÄÉÖÜßÀÂÆÇÈÉÊËÎÏÔŒÙÛÜŸ"
  }
  # Loaded module rlm_passwd
  # Loading module "etc_passwd" from file /etc/freeradius/mods-enabled/passwd
  passwd etc_passwd {
  	filename = "/etc/passwd"
  	format = "*User-Name:Crypt-Password:"
  	delimiter = ":"
  	ignore_nislike = no
  	ignore_empty = yes
  	allow_multiple_keys = no
  	hash_size = 100
  }
  # Loading module "exec" from file /etc/freeradius/mods-enabled/exec
  exec {
  	wait = no
  	input_pairs = "request"
  	shell_escape = yes
  	timeout = 10
  }
  # Loaded module rlm_date
  # Loading module "date" from file /etc/freeradius/mods-enabled/date
  date {
  	format = "%b %e %Y %H:%M:%S %Z"
  	utc = no
  }
  # Loading module "wispr2date" from file /etc/freeradius/mods-enabled/date
  date wispr2date {
  	format = "%Y-%m-%dT%H:%M:%S"
  	utc = no
  }
  # Loaded module rlm_files
  # Loading module "files" from file /etc/freeradius/mods-enabled/files
  files {
  	filename = "/etc/freeradius/mods-config/files/authorize"
  	acctusersfile = "/etc/freeradius/mods-config/files/accounting"
  	preproxy_usersfile = "/etc/freeradius/mods-config/files/pre-proxy"
  }
  # Loaded module rlm_unpack
  # Loading module "unpack" from file /etc/freeradius/mods-enabled/unpack
  # Loaded module rlm_expiration
  # Loading module "expiration" from file /etc/freeradius/mods-enabled/expiration
  # Loaded module rlm_utf8
  # Loading module "utf8" from file /etc/freeradius/mods-enabled/utf8
  # Loaded module rlm_pap
  # Loading module "pap" from file /etc/freeradius/mods-enabled/pap
  pap {
  	normalise = yes
  }
  # Loaded module rlm_ldap
  # Loading module "ldap" from file /etc/freeradius/mods-enabled/ldap
  ldap {
  	server = "ldap.server.rlik"
  	identity = "cn=admin,dc=ldap,dc=server,dc=rlik"
  	password = <<< secret >>>
   sasl {
   }
  	user_dn = "LDAP-UserDn"
   user {
   	scope = "sub"
   	access_positive = yes
    sasl {
    }
   }
   group {
   	filter = "(objectClass=posixGroup)"
   	scope = "sub"
   	name_attribute = "cn"
   	membership_attribute = "memberOf"
   	cacheable_name = no
   	cacheable_dn = no
   	allow_dangling_group_ref = no
   }
   client {
   	filter = "(objectClass=radiusClient)"
   	scope = "sub"
   	base_dn = "dc=ldap,dc=server,dc=rlik"
   }
   profile {
   }
   options {
   	ldap_debug = 40
   	chase_referrals = yes
   	rebind = yes
   	net_timeout = 1
   	res_timeout = 10
   	srv_timelimit = 3
   	idle = 60
   	probes = 3
   	interval = 3
   }
   tls {
   	cipher_list = "DEFAULT"
   	check_crl = no
   	start_tls = no
   }
  }
Creating attribute LDAP-Group
  instantiate {
  }
  # Instantiating module "IPASS" from file /etc/freeradius/mods-enabled/realm
  # Instantiating module "suffix" from file /etc/freeradius/mods-enabled/realm
  # Instantiating module "bangpath" from file /etc/freeradius/mods-enabled/realm
  # Instantiating module "realmpercent" from file /etc/freeradius/mods-enabled/realm
  # Instantiating module "ntdomain" from file /etc/freeradius/mods-enabled/realm
  # Instantiating module "detail" from file /etc/freeradius/mods-enabled/detail
  # Instantiating module "linelog" from file /etc/freeradius/mods-enabled/linelog
  # Instantiating module "log_accounting" from file /etc/freeradius/mods-enabled/linelog
  # Instantiating module "auth_log" from file /etc/freeradius/mods-enabled/detail.log
rlm_detail (auth_log): 'User-Password' suppressed, will not appear in detail output
  # Instantiating module "reply_log" from file /etc/freeradius/mods-enabled/detail.log
  # Instantiating module "pre_proxy_log" from file /etc/freeradius/mods-enabled/detail.log
  # Instantiating module "post_proxy_log" from file /etc/freeradius/mods-enabled/detail.log
  # Instantiating module "reject" from file /etc/freeradius/mods-enabled/always
  # Instantiating module "fail" from file /etc/freeradius/mods-enabled/always
  # Instantiating module "ok" from file /etc/freeradius/mods-enabled/always
  # Instantiating module "handled" from file /etc/freeradius/mods-enabled/always
  # Instantiating module "invalid" from file /etc/freeradius/mods-enabled/always
  # Instantiating module "userlock" from file /etc/freeradius/mods-enabled/always
  # Instantiating module "notfound" from file /etc/freeradius/mods-enabled/always
  # Instantiating module "noop" from file /etc/freeradius/mods-enabled/always
  # Instantiating module "updated" from file /etc/freeradius/mods-enabled/always
  # Instantiating module "preprocess" from file /etc/freeradius/mods-enabled/preprocess
reading pairlist file /etc/freeradius/mods-config/preprocess/huntgroups
reading pairlist file /etc/freeradius/mods-config/preprocess/hints
  # Instantiating module "attr_filter.post-proxy" from file /etc/freeradius/mods-enabled/attr_filter
reading pairlist file /etc/freeradius/mods-config/attr_filter/post-proxy
  # Instantiating module "attr_filter.pre-proxy" from file /etc/freeradius/mods-enabled/attr_filter
reading pairlist file /etc/freeradius/mods-config/attr_filter/pre-proxy
  # Instantiating module "attr_filter.access_reject" from file /etc/freeradius/mods-enabled/attr_filter
reading pairlist file /etc/freeradius/mods-config/attr_filter/access_reject
  # Instantiating module "attr_filter.access_challenge" from file /etc/freeradius/mods-enabled/attr_filter
reading pairlist file /etc/freeradius/mods-config/attr_filter/access_challenge
  # Instantiating module "attr_filter.accounting_response" from file /etc/freeradius/mods-enabled/attr_filter
reading pairlist file /etc/freeradius/mods-config/attr_filter/accounting_response
  # Instantiating module "attr_filter.coa" from file /etc/freeradius/mods-enabled/attr_filter
reading pairlist file /etc/freeradius/mods-config/attr_filter/coa
  # Instantiating module "logintime" from file /etc/freeradius/mods-enabled/logintime
  # Instantiating module "mschap" from file /etc/freeradius/mods-enabled/mschap
rlm_mschap (mschap): using internal authentication
  # Instantiating module "etc_passwd" from file /etc/freeradius/mods-enabled/passwd
rlm_passwd: nfields: 3 keyfield 0(User-Name) listable: no
  # Instantiating module "files" from file /etc/freeradius/mods-enabled/files
reading pairlist file /etc/freeradius/mods-config/files/authorize
reading pairlist file /etc/freeradius/mods-config/files/accounting
reading pairlist file /etc/freeradius/mods-config/files/pre-proxy
  # Instantiating module "expiration" from file /etc/freeradius/mods-enabled/expiration
  # Instantiating module "pap" from file /etc/freeradius/mods-enabled/pap
  # Instantiating module "ldap" from file /etc/freeradius/mods-enabled/ldap
rlm_ldap: libldap vendor: OpenLDAP, version: 20516
   accounting {
   	reference = "%{tolower:type.%{Acct-Status-Type}}"
   }
   post-auth {
   	reference = "."
   }
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
!! libldap is using GnuTLS, while FreeRADIUS is using OpenSSL
!! There may be random issues with TLS connections due to this conflict.
!! The server may also crash.
!! See https://wiki.freeradius.org/modules/Rlm_ldap for more information.
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
rlm_ldap (ldap): Initialising connection pool
   pool {
   	start = 5
   	min = 3
   	max = 32
   	spare = 10
   	uses = 0
   	lifetime = 0
   	cleanup_interval = 30
   	idle_timeout = 60
   	retry_delay = 30
   	max_retries = 5
   	spread = no
   }
rlm_ldap (ldap): Opening additional connection (0), 1 of 32 pending slots used
rlm_ldap (ldap): Connecting to ldap://ldap.server.rlik:389
rlm_ldap (ldap): Waiting for bind result...
rlm_ldap (ldap): Bind successful
rlm_ldap (ldap): Opening additional connection (1), 1 of 31 pending slots used
rlm_ldap (ldap): Connecting to ldap://ldap.server.rlik:389
rlm_ldap (ldap): Waiting for bind result...
rlm_ldap (ldap): Bind successful
rlm_ldap (ldap): Opening additional connection (2), 1 of 30 pending slots used
rlm_ldap (ldap): Connecting to ldap://ldap.server.rlik:389
rlm_ldap (ldap): Waiting for bind result...
rlm_ldap (ldap): Bind successful
rlm_ldap (ldap): Opening additional connection (3), 1 of 29 pending slots used
rlm_ldap (ldap): Connecting to ldap://ldap.server.rlik:389
rlm_ldap (ldap): Waiting for bind result...
rlm_ldap (ldap): Bind successful
rlm_ldap (ldap): Opening additional connection (4), 1 of 28 pending slots used
rlm_ldap (ldap): Connecting to ldap://ldap.server.rlik:389
rlm_ldap (ldap): Waiting for bind result...
rlm_ldap (ldap): Bind successful
 } # modules
radiusd: #### Loading Virtual Servers ####
server { # from file /etc/freeradius/radiusd.conf
} # server
server my_server { # from file /etc/freeradius/sites-enabled/my_server
 # Loading authenticate {...}
Compiling Auth-Type LDAP for attr Auth-Type
 # Loading authorize {...}
} # server my_server
radiusd: #### Opening IP addresses and Ports ####
listen {
  	type = "auth"
  	ipaddr = *
  	port = 1815
}
Listening on auth address * port 1815 bound to server my_server
Listening on proxy address * port 39434
Ready to process requests
