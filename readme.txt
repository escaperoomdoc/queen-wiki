# common
apt update && sudo apt upgrade -y
apt install mc
apt install nano
# appache (if not installed)
sudo apt install apache2
sudo systemctl stop apache2.service
sudo systemctl start apache2.service
sudo systemctl enable apache2.service
# php7.0
sudo apt install -y php7.0 php7.0-cli php7.0-fpm php7.0-gd php7.0-xml php7.0-zip
#doku
sudo mkdir -p /var/www/dokuwiki
cd /var/www/dokuwiki
wget https://download.dokuwiki.org/src/dokuwiki/dokuwiki-stable.tgz
tar xvf dokuwiki-stable.tgz
rm dokuwiki-stable.tgz
# перенести содержимое папки dokuwiki в /var/www/html
...
# restart php
apt-get install libapache2-mod-php
systemctl restart php7.0-fpm.service
# restart
sudo reboot
