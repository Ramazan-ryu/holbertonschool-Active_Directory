README.md

TASK 0 
Get-ADObject (Get-ADDomain).DistinguishedName -Properties *


TASK 1
In kali 
vim /etc/hosts
192.168.56.20   pentestlab.local
192.168.56.20   DC01.pentestlab.local

than
ldapsearch -x -H ldap://DC01.pentestlab.local -b "dc=pentestlab,dc=local" "(objectClass=*)"
