root@0aa2805d9b1f:/# radtest test test radius 0 qqqqqqqq
Sent Access-Request Id 135 from 0.0.0.0:ecfb to 172.28.0.3:1812 length 74
	User-Name = "test"
	User-Password = "test"
	NAS-IP-Address = 172.28.0.3
	NAS-Port = 0
	Message-Authenticator = 0x00
	Cleartext-Password = "test"
Received Access-Reject Id 135 from 172.28.0.3:714 to 172.28.0.3:60667 length 20
(0) -: Expected Access-Accept got Access-Reject
