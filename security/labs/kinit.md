[root@instance-8 ~]# kinit root
Password for root@EXAMPLE.COM:
[root@instance-8 ~]# klist -e
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: root@EXAMPLE.COM

Valid starting       Expires              Service principal
10/18/2018 08:01:23  10/19/2018 08:01:23  krbtgt/EXAMPLE.COM@EXAMPLE.COM
        Etype (skey, tkt): aes256-cts-hmac-sha1-96, aes256-cts-hmac-sha1-96
[root@instance-8 ~]#
