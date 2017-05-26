# Ujian-Devops
# devOps Ujian
## Batch001 20170526
#### Indra Purnomo
## SOAL : Bagaimanakah cara memasang web dari repo ini di server? |
Alamat Repo: https://github.com/BlankOn/blankon-linux-static-web
#### Berikut  langkah langkahnya :
* Pertama kita buat dulu repo baru di akun github kita, misal punya saya nama reponya Ujian Devops
* Pertama kita clone dulu reponya di Alamat tadi dengan git clone [alamat]
* Kemudian buat folder nama ujianvagrant dan ketikkan perintah vagrant init |
Untuk membuat vagrantfile yang akan kita konfigurasi
* Copy dan pastekan file yang sudah anda clone tadi ke folder ujianvagrant
* Kemudian buka file vagrantfile dengan editor yang ada di linux misal sublimetext
* Lalu konfigurasi mesin anda
* konfigurasi Provision kita akan mengatur penginstalan dsb,sebelumnya kita buat file install.sh di folder ujianvagrant
#!/usr/bin/env bash
echo "Mulai Provisioning"    
echo "Mulai Update"
sudo apt-get update
echo "Instalasi Nginx,curl,vim"
sudo apt-get install -y nginx curl vim

echo "Nginx Config"
sudo rm -rf /var/www/index.nginx-debian.html
sudo cp -r /vagrant/blankon-linux-static-web/index.html /var/www/html
