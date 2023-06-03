# Helpful Commands
## random commands

Hkar8Sybek!

scp eightbitoni@5.5.5.134:ovpns/eightbitoni.ovpn /home/eightbitoni/Downloads

scp eightbitoni@5.5.5.134:configs/Oni.conf /home/eightbitoni/Desktop

## quick notes
apt-cache search nameofprogram

hexdump -C 123.txt

ll
ls -a
ls -al
ls -l

grep in a .txt or file
grep word 123.txt

entire directory
grep file -r
example
grep -r "mission22 > /dev/null


ssh -i id_rsa cactus@10.10.164.165

---

chmod +x yourfile.sh

ls -l -check on permissions for file  
For **owner** it is 4+2+1=7 (111 in binary)  
For **group** it is 4+0+1=5 (101 in binary) and  
For **other** it is 4+0+1=5 (101 in binary).  
make it executable with $ chmod +x warm

---

decode base 64
echo "fWZhYTk0ZDI0YjQ4OTZlMmE2ZGU5ODgwYmU0N2FhYzQyezIybm9pc3NpbQo="|base64 -d|re  
v  

---

python3 -m http.server

---

wget http://x.x.x.x:8000/file

---
this is how to make a reverse shell look normal with color

export TERM=xterm-256color

---

sudo /etc/init.d/bluetooth start

---

systemctl start bluetooth.service

---

wget - install from website with link

---

view last few lines command in file

tail [OPTION]... [FILE]...
ex
tail -n 5 filename

head shows first lines
