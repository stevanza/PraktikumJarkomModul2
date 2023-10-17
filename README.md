# PraktikumJarkomModul2
1. Yudhistira akan digunakan sebagai DNS Master, Werkudara sebagai DNS Slave, Arjuna merupakan Load Balancer yang terdiri dari beberapa Web Server yaitu Prabakusuma, Abimanyu, dan Wisanggeni. Buatlah topologi dengan pembagian sebagai berikut.
![soal](https://github.com/stevanza/PraktikumJarkomModul2/blob/main/WhatsApp%20Image%202023-10-17%20at%2018.42.38_ef3e9851.jpg)


3. Buatlah website utama pada node arjuna dengan akses ke arjuna.yyy.com dengan alias www.arjuna.yyy.com dengan yyy merupakan kode kelompok.
Buka Arjuna dan jalankan command  apt-get update
![soal](https://github.com/stevanza/PraktikumJarkomModul2/blob/main/WhatsApp%20Image%202023-10-17%20at%2018.52.33_e02e7588.jpg)
setelah melakukan update install aplikasi bind9 pada Arjuna
![soal](https://github.com/stevanza/PraktikumJarkomModul2/blob/main/WhatsApp%20Image%202023-10-17%20at%2018.55.55_2408d531.jpg)
lakukan perintah pada Arjuna menggunakan command nano /etc/bind/named.conf.local
isikan konfigurasi domain arjuna.e05.com dengan syntax
zone "arjuna.e05.com" {
	type master;
	file "/etc/bind/jarkom/arjuna.e05.com";
};
![soal](https://github.com/stevanza/PraktikumJarkomModul2/blob/main/WhatsApp%20Image%202023-10-17%20at%2018.57.50_6472720c.jpg)
lalu buatkan folder jarkom dengan command mkdir /etc/bind/jarkom
![soal](https://github.com/stevanza/PraktikumJarkomModul2/blob/main/WhatsApp%20Image%202023-10-17%20at%2019.22.58_45b7f1a6.jpg)
Copykan file db.local pada path /etc/bind ke dalam folder jarkom yang baru saja dibuat dan ubah namanya menjadi arjuna.e05.com
cp /etc/bind/db.local /etc/bind/jarkom/arjuna.e05.com
kemudian buka file arjuna.e05.com dan edit ip sesuai dengan kelompok masing masing
nano /etc/bind/jarkom/arjuna.e05.com
![soal](https://github.com/stevanza/PraktikumJarkomModul2/blob/main/WhatsApp%20Image%202023-10-17%20at%2019.23.23_b71a6c54.jpg)
![soal](https://github.com/stevanza/PraktikumJarkomModul2/blob/main/WhatsApp%20Image%202023-10-17%20at%2019.06.30_afb9872e.jpg)
setelah itu restart bind9 dengan command service bind9 restart
![soal](https://github.com/stevanza/PraktikumJarkomModul2/blob/main/WhatsApp%20Image%202023-10-17%20at%2019.08.16_75df1035.jpg)

