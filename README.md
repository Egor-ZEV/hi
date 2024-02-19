root@cf649877b739:/etc/freeradius/mods-enabled# radtest test1 testpassword 127.0.0.1:1812 0  testing123
Sent Access-Request Id 165 from 0.0.0.0:b1ac to 127.0.0.1:1812 length 75
	User-Name = "test1"
	User-Password = "testpassword"
	NAS-IP-Address = 172.28.0.7
	NAS-Port = 0
	Message-Authenticator = 0x00
	Cleartext-Password = "testpassword"
Received Access-Reject Id 165 from 127.0.0.1:714 to 127.0.0.1:45484 length 20
(0) -: Expected Access-Accept got Access-Reject
