Tue Feb 20 10:56:19 2024 : Info: Debug state unknown (cap_sys_ptrace capability not set)
Tue Feb 20 10:56:19 2024 : Info: systemd watchdog is disabled
Tue Feb 20 10:56:19 2024 : Info: rlm_ldap: libldap vendor: OpenLDAP, version: 20514
Tue Feb 20 10:56:19 2024 : Warning: !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
Tue Feb 20 10:56:19 2024 : Warning: !! libldap is using GnuTLS, while FreeRADIUS is using OpenSSL
Tue Feb 20 10:56:19 2024 : Warning: !! There may be random issues with TLS connections due to this conflict.
Tue Feb 20 10:56:19 2024 : Warning: !! The server may also crash.
Tue Feb 20 10:56:19 2024 : Warning: !! See https://wiki.freeradius.org/modules/Rlm_ldap for more information.
Tue Feb 20 10:56:19 2024 : Warning: !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
Tue Feb 20 10:56:19 2024 : Info: Loaded virtual server <default>
Tue Feb 20 10:56:19 2024 : Warning: Ignoring "sql" (see raddb/mods-available/README.rst)
Tue Feb 20 10:56:19 2024 : Info:  # Skipping contents of 'if' as it is always 'false' -- /etc/freeradius/sites-enabled/inner-tunnel:366
Tue Feb 20 10:56:19 2024 : Info: Loaded virtual server inner-tunnel
Tue Feb 20 10:56:19 2024 : Info: Loaded virtual server default
Tue Feb 20 10:56:19 2024 : Error: Failed binding to auth address 127.0.0.1 port 1812 bound to server inner-tunnel: Address already in use
Tue Feb 20 10:56:19 2024 : Error: /etc/freeradius/sites-enabled/inner-tunnel[33]: Error binding to port for 127.0.0.1 port 1812
