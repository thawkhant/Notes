
gobuster dir -u http://workers.htb -w /usr/share/dirbuster/wordlists/directory-list-2.3-medium.txt -x php,php3,html,txt       => brute force for dir

I see the place for command injection

grep -R .   => i inject like this


rabbit hole    => result i decode with base 64 for many times