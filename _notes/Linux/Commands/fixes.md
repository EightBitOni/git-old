if unable to locate package update try

sudo dpkg --configure -a
sudo apt install -f

sudo apt install update && sudo apt install upgrade -y
	or
sudo apt install update -y && sudo apt install upgrade -y
	or
sudo apt update -y && sudo apt upgrade -y

sudo apt clean
sudo apt update
sudo apt install -f

openvpn issues
`sed -i 's/cipher AES-256-CBC/data-ciphers AES-256-CBC/' *.ovpn`


sudo apt autoremove

------------------

initramfs
fsck <your file system path> -y
	
fixing kernal panic init not found
sudo update-initramfs -u

	
sudo fdisk -l
fsck /dev/sda1 -y
	
------------------------------------
	
dpkg error: parsing file '/var/lib/dpkg/status' near line 28403 package 'liblockfile-bin' :

sudo rm /var/lib/dpkg/status
sudo cp /var/backups/dpkg.status.0 /var/lib/dpkg/status
sudo apt-get update

	


