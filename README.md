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

![soal](https://github.com/stevanza/PraktikumJarkomModul2/blob/main/WhatsApp%20Image%202023-10-17%20at%2019.00.05_704e524c.jpg)
