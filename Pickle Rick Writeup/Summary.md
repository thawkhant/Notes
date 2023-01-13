
gobuster dir -u http://workers.htb -w /usr/share/dirbuster/wordlists/directory-list-2.3-medium.txt -x php,php3,html,txt       => brute force for dir

I see the place for command injection

username => R1ckRul3s   / i got from source code
password  => Wubbalubbadubdub / i got feom robots.txt

grep -R .   => i inject like this


rabbit hole    => result i decode with base 64 for many times