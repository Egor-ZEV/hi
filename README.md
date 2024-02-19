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
 } # modules
radiusd: #### Loading Virtual Servers ####
server { # from file /etc/freeradius/radiusd.conf
} # server
server my_server { # from file /etc/freeradius/sites-enabled/my_server
 # Loading authenticate {...}
Compiling Auth-Type PAP for attr Auth-Type
Compiling Auth-Type CHAP for attr Auth-Type
 # Loading authorize {...}
} # server my_server
radiusd: #### Opening IP addresses and Ports ####
listen {
  	type = "auth"
  	ipaddr = *
  	port = 1812
Failed binding to auth address * port 1812 bound to server my_server: Address already in use 
/etc/freeradius/sites-enabled/my_server[2]: Error binding to port for 0.0.0.0 port 1812
