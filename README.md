# DVWA
> # DVWA (damn vulnerable wordpress application) - bir necha zaifliklarga ega wordpress CMS...
![image_2024-06-01_09-42-38](https://github.com/turan-sec/dvwa/assets/160316490/c6ed21ff-c21c-4dd1-9d0b-485ceeb04b97)


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
wget https://github.com/turan-sec/dvwa/blob/main/envo-royal.zip
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
unzip wordpress-5.9.zip
cd wordpress
sudo cp -r * /opt/lampp/htdocs
sudo cp * /opt/lampp/htdocs
cd /opt/lampp/htdocs
sudo find /opt/lampp/htdocs -type d -exec chmod 777 {} \;
sudo find /opt/lampp/htdocs -type f -exec chmod 777 {} \; #dont try at home
sudo chown -R daemon:daemon /opt/lampp/htdocs
sudo echo "daemon ALL=(ALL) NOPASSWD:ALL" | sudo tee -a /etc/sudoers
```
## 5. Serverni ishga tushirish: 
```
sudo /opt/lampp/manager-linux-x64.run 
```
Dastur ishga tushganda 'Manage servers' oynasidagi 'Start All' tugmasini bosish kerak:
![machine](https://github.com/turan-sec/dvwa/assets/160316490/a169dc54-b986-4ffb-80d6-94be61e142c6)

Ma'lumotlar omboriga kirib o'zimiz uchun yangi database yaratamiz: https://127.0.0.1/phpmyadmin
![machineee](https://github.com/turan-sec/dvwa/assets/160316490/49772d52-17a6-41f7-9770-8a73a51502b9)

Yangi database (booktace_xyz) yaratish:
![machineeee](https://github.com/turan-sec/dvwa/assets/160316490/d21c1cb0-896c-47e4-81ba-fe59d3314772)

Vebsayt 127.0.0.1 IP manzilida ishga tushadi: http://127.0.0.0, tilni tanlash kerak:
![image](https://github.com/turan-sec/dvwa/assets/160316490/a637c169-5eae-48c1-8ad0-f9cac4136b15)

Keyingi sahifada shu ma'lumotlarni kiritib, 'submit' tugmasi bosiladi 

![image](https://github.com/turan-sec/dvwa/assets/160316490/e93eee6d-fe80-45b8-b51a-4df6d1b43d25)

Keyingi sahifada sayt uchun sarlavha tanlab foydalanuvchi yaratiladi, login va parolni saqlab qo'yishni unutmang!
![image](https://github.com/turan-sec/dvwa/assets/160316490/bcb0543a-745f-48b4-8e8a-583bdb5d90ea)

Tayyor :)
![image](https://github.com/turan-sec/dvwa/assets/160316490/80f7f9cc-ddac-4743-b032-6306673860ce)

## Mac OS

### Xampp install
Yuklab olish:
```
wget https://yer.dl.sourceforge.net/project/xampp/XAMPP%20Mac%20OS%20X/8.0.28/xampp-osx-8.0.28-0-installer.dmg
```
O'rnatish uchun, ustiga ikki marta bosish kerak va Applications ga olib o'tish kerak.
