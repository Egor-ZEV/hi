docker stop ldap_ui
docker rm ldap_ui
docker run --log-opt max-size=10m --log-opt max-file=3 -d --name ldap_ui -p 5000:5000 --network testnet dnknth/ldap-ui:latest
