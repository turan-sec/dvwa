# DVWA
> # DVWA (damn vulnerable wordpress application) - bir necha zaifliklarga ega wordpress CMS...
![3840x2160-harry-potter-following-the-darkness-4k_1606594935](https://github.com/turan-sec/dvwa/assets/160316490/c64c80fe-1a38-4e79-a94b-9d2207a54501)

## 1. Kerakli fayllarni yuklab olish (Debian - Ubuntu, Kali Linux, etc):
```
mkdir ~/Downloads/dvwa & cd ~/Downloads/dvwa
```
Wordpress:
```
wget https://wordpress.org/wordpress-5.9.zip
```
Pluginlar:
```
wget https://codeload.github.com/wp-plugins/404-to-301/zip/refs/tags/2.0.1
```
```
wget https://downloads.wordpress.org/plugin/ultimate-member.2.1.11.zip
```
```
wget https://downloads.wordpress.org/plugin/imagemagick-engine.1.7.4.zip
```
Wordpress theme:
```
wget https://redacted
```
Xampp (Apache, MySQL, ProFTPD):
```
wget https://sourceforge.net/projects/xampp/files/XAMPP%20Linux/8.0.30/xampp-linux-x64-8.0.30-0-installer.run
```
## 2. O'rnatish:
```
chmod +766 sudo xampp-linux-x64-8.0.30-0-installer.run & sudo ./xampp-linux-x64-8.0.30-0-installer.run
```
Nextlar...
## 3. Sozlamalar:
```
sudo apt install ncat
cd /opt/lampp/htdocs
sudo mkdir dash2
sudo mv * dash2
cd ~/Downloads/dvwa
unzip wordpress-5.9.zip .
cd wordpress
sudo cp -r * /opt/lampp/htdocs
sudo cp * /opt/lampp/htdocs
cd /opt/lampp/htdocs
sudo touch wp-config.php
```
