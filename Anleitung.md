
# Anleitung zur installation

abweichend von dem fork und den Docs im Ordner "docs" eine Anleitung wie ich mein rapsberry eingerichtet habe.

# ssh einrichten für Github

1. Keypaar erstellen mit
   1. `ssh-keygen -t ed25519 -C mail@mail.com`
      1. wichtig beim angeben des namens den pfad gleich wählen. /home/pi/.ssh/"id name ohne zeichen"
      2. danach passphrase eingeben oder ein kennwort. gut merken.
   2. `ssh-add ~/.ssh/"id name"` & Passwort
   3. ~/.ssh/id name.pub öffnen und bei github eintragen. fertig

ssh-keygen commands \

1. **-t ed25519**"\
"-t “Type” This option specifies the type of key to be created. Commonly used values are: - rsa for RSA keys - dsa for DSA keys - ed25519 keys"\
2. **-C** is comment.

## Verschiedenes

/home/pi/config_programme/homer
sudo chown -R 1000:1000 /home/pi/config_programme/Homer/

sudo chmod -R u+rw /home/pi/config_programme/Homer/

für Festplatte
sudo apt-get install gnome-disk-utility -y && apt-get install ntfs-3g -y
danach checken wir den ordner /media ob die fetstplatte da ist
interessanter [link](https://pimylifeup.com/raspberry-pi-mount-usb-drive/)
> list all drivers\
> sudo blkid\
> sudo mount /dev/sda1/"folder" /mnt\
> sudo chmod 775 /mnt\

## falls was schief geht

sudo apt-get install xrdp \
sudo apt-get remove xrdp vnc4server tightvncserver --yes \
sudo apt-get install tightvncserver -y \

To see a list of all users, use
cat /etc/passwd

all logins
lslogins -u
/portainer/Files/AppData/Config/Plex
/portainer/Files/AppData/Config/"container name"
# Ablauf

list of all in one install package
gnome-disk-utility, ntfs-3g, git

1. cd Downloads
2. sudo mkdir pi-hosted
3. install
   1. git
   2. ntfs-3g 
   3. gnome-disk-utility
   4. install docker via script
   5. install portainer via script
   6. create file directory for docker
   7. install my favorite