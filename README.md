# ch-linux-codes
linux codes
HOW TO SSH WITH PRIVATE SUBNET (SERVER)
Using username "ec2-user".
Authenticating with public key "imported-openssh-key"
Last login: Sun Mar 15 21:47:31 2020 from 76.106.103.109

       __|  __|_  )
       _|  (     /   Amazon Linux 2 AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-2/
1 package(s) needed for security, out of 1 available
Run "sudo yum update" to apply all updates.
[ec2-user@ip-10-0-1-133 ~]$ sudo su -
Last login: Sun Mar 15 22:25:38 UTC 2020 on pts/0
[root@ip-10-0-1-133 ~]# vi ch.pem
[root@ip-10-0-1-133 ~]# ssh -i "ch.pem" ec2-user@ec2-34-238-232-202.compute-1.amazonaws.com
The authenticity of host 'ec2-34-238-232-202.compute-1.amazonaws.com (10.0.0.68)' can't be established.
ECDSA key fingerprint is SHA256:RPiGfnkA72fGzs0Mbj9kbcIIrsGcdClKf8T9htFJ6nY.
ECDSA key fingerprint is MD5:58:b5:80:f2:24:37:39:f9:65:69:bf:33:08:c4:2b:c1.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'ec2-34-238-232-202.compute-1.amazonaws.com,10.0.0.68' (ECDSA) to the list of known hosts.
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0644 for 'ch.pem' are too open.
It is required that your private key files are NOT accessible by others.
This private key will be ignored.
Load key "ch.pem": bad permissions
Permission denied (publickey,gssapi-keyex,gssapi-with-mic).
[root@ip-10-0-1-133 ~]# ls
ch.pem
[root@ip-10-0-1-133 ~]# chmod 400 ch.pem
[root@ip-10-0-1-133 ~]# ssh -i "ch.pem" ec2-user@ec2-34-238-232-202.compute-1.amazonaws.com

       __|  __|_  )
       _|  (     /   Amazon Linux 2 AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-2/
[ec2-user@ip-10-0-0-68 ~]$

