

export IP=192.168.99.105

nmap -sC -sV $IP

=> Use msfconsole and check ftp version is exploit or not

searchsploit vsftpd 3.0.3    => Check with manual

ftp 192.168.99.105   => i try to connect with ftp but  its fail!

site help      => i also use this command to enumate

smbmap -H 192.168.99.105     => cuz i found smbp port in 445

smbclient //192.168.99.105/anonymous -N   => cuz i found anonymous file 

get share  => i downloaded share file

![[Pasted image 20230109212959.png]]

I get this information from share file that i downloaded  => include ftp username and password


hash-identifier    => i try to know which hashing algoram use for hashing

https://hashes.com/en/decrypt/hash   => decrypt

Finally i found user name and password for FTP server 
-> admin
->qazwsxedc

 cd /     => go to root  dictory   => we get user access


----------------------------------

SSH username and password also same with FTP service



