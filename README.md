docker run -p 127.0.0.1:5000:5000 \
  -e LDAP_URL=ldap://your.ldap.server/ \
  -e BASE_DN=dc=example,dc=org dnknth/ldap-ui
