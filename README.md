<h1>Praktikum Modul 3 Jaringan Komputer</h1>
<h3>Kelompok I07</h3>

| NAME                          | NRP       |
|-------------------------------|-----------|
|Pascal Roger Junior Tauran     |5025211072 |
|Mochammad Naufal Ihza Syahzada |5025211260 |

## Number 1
```
Semua CLIENT harus menggunakan konfigurasi dari DHCP Server.
```

Tapology:<br>
![Modul3Tapology](https://cdn.discordapp.com/attachments/824131614073683968/1174607666132291614/image.png?ex=656835a2&is=6555c0a2&hm=99e647e784aa83f2a45506418f22f9f5a69d66c83bd960e8a05eba0917ac405c&)

### Aura
```bash
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.62.1.1
	netmask 255.255.255.0

auto eth2
iface eth2 inet static
	address 10.62.2.1
	netmask 255.255.255.0

auto eth3
iface eth3 inet static
	address 10.62.3.1
	netmask 255.255.255.0

auto eth4
iface eth4 inet static
	address 10.62.4.1
	netmask 255.255.255.0
```
### Revolte
```bash
auto eth0
iface eth0 inet dhcp
#	address 10.62.3.2
#	netmask 255.255.255.0
#	gateway 10.62.3.1
```
### Richter
```bash
auto eth0
iface eth0 inet dhcp
#	address 10.62.3.3
#	netmask 255.255.255.0
#	gateway 10.62.3.1
```
### Lawine
```bash
auto eth0
iface eth0 inet static
	address 10.62.3.4
	netmask 255.255.255.0
	gateway 10.62.3.1
```
### Linle
```bash
auto eth0
iface eth0 inet static
	address 10.62.3.5
	netmask 255.255.255.0
	gateway 10.62.3.1
```
### Lugner
```bash
auto eth0
iface eth0 inet static
	address 10.62.3.6
	netmask 255.255.255.0
	gateway 10.62.3.1
```
### Sein
```bash
auto eth0
iface eth0 inet dhcp
#	address 10.62.4.2
#	netmask 255.255.255.0
#	gateway 10.62.4.1
```
### Stark
```bash
auto eth0
iface eth0 inet dhcp
#	address 10.62.4.3
#	netmask 255.255.255.0
#	gateway 10.62.4.1
```
### Freiren
```bash
auto eth0
iface eth0 inet static
	address 10.62.4.4
	netmask 255.255.255.0
	gateway 10.62.4.1
```
### Flamme
```bash
auto eth0
iface eth0 inet static
	address 10.62.4.5
	netmask 255.255.255.0
	gateway 10.62.4.1
```
### Fern
```bash
auto eth0
iface eth0 inet static
	address 10.62.4.6
	netmask 255.255.255.0
	gateway 10.62.4.1
```
### Himmel
```bash
auto eth0
iface eth0 inet static
	address 10.62.1.2
	netmask 255.255.255.0
	gateway 10.62.1.1
```
### Heiter
```bash
auto eth0
iface eth0 inet static
	address 10.62.1.3
	netmask 255.255.255.0
	gateway 10.62.1.1
```
### Denken
```bash
auto eth0
iface eth0 inet static
	address 10.62.2.2
	netmask 255.255.255.0
	gateway 10.62.2.1
```
### Elsen
```bash
auto eth0
iface eth0 inet static
	address 10.62.2.3
	netmask 255.255.255.0
	gateway 10.62.2.1
```
## Number 2
```
Client yang melalui Switch3 mendapatkan range IP dari [prefix IP].3.16 - [prefix IP].3.32 dan [prefix IP].3.64 - [prefix IP].3.80 (2)
```
- `/etc/dhcp/dhcpd.conf` `Himmel`
```bash
subnet 10.62.3.0 netmask 255.255.255.0 {
    range 10.62.3.16 10.62.3.32;
    range 10.62.3.64 10.62.3.80;
    option routers 10.62.3.1;
    option broadcast-address 10.62.3.255;
    option domain-name-servers 10.62.1.3;
    default-lease-time 600;
    max-lease-time 7200; 
}
```
- `bashrc` `Himmel` <br>
![bashrc_Himmel](https://cdn.discordapp.com/attachments/824131614073683968/1174694205751300096/image.png?ex=6568863b&is=6556113b&hm=8db1cf31e064bc55c246cadea5acc3844f4aaa6270e5b86a68bceedf08323106&)

- `terminal` `Himmel` <br>
![terminal_Himmel](https://cdn.discordapp.com/attachments/824131614073683968/1174695490802176040/image.png?ex=6568876d&is=6556126d&hm=09709c2b7a4a50a6ffb2870a86c649fa275f3880e72f931852b2ca8f3dba619d&)

## Number 3
```
Client yang melalui Switch4 mendapatkan range IP dari [prefix IP].4.12 - [prefix IP].4.20 dan [prefix IP].4.160 - [prefix IP].4.168 (3)
```
- `/etc/dhcp/dhcpd.conf`
```bash
subnet 10.62.4.0 netmask 255.255.255.0 {
    range 10.62.4.12 10.62.4.20;
    range 10.62.4.160 10.62.4.168;
    option routers 10.62.4.1;
    option broadcast-address 10.62.4.255;
    option domain-name-servers 10.62.1.3;
    default-lease-time 600;
    max-lease-time 7200;
}
```
- `bashrc` `Himmel` <br>
![bashrc_Himmel](https://cdn.discordapp.com/attachments/824131614073683968/1174694205751300096/image.png?ex=6568863b&is=6556113b&hm=8db1cf31e064bc55c246cadea5acc3844f4aaa6270e5b86a68bceedf08323106&)

- `terminal` `Himmel` <br>
![terminal_Himmel](https://cdn.discordapp.com/attachments/824131614073683968/1174695490802176040/image.png?ex=6568876d&is=6556126d&hm=09709c2b7a4a50a6ffb2870a86c649fa275f3880e72f931852b2ca8f3dba619d&)

## Number 4
```
Client mendapatkan DNS dari Heiter dan dapat terhubung dengan internet melalui DNS tersebut (4)
```
- `/etc/dhcp/dhcpd.conf`
```bash
echo subnet 10.62.1.0 netmask 255.255.255.0 {
}

subnet 10.62.4.0 netmask 255.255.255.0 {
    range 10.62.4.12 10.62.4.20;
    range 10.62.4.160 10.62.4.168;
    option routers 10.62.4.1;
    option broadcast-address 10.62.4.255;
    option domain-name-servers 10.62.1.3;
    #default-lease-time 600;
    #max-lease-time 7200;
}

subnet 10.62.3.0 netmask 255.255.255.0 {
    range 10.62.3.16 10.62.3.32;
    range 10.62.3.64 10.62.3.80;
    option routers 10.62.3.1;
    option broadcast-address 10.62.3.255;
    option domain-name-servers 10.62.1.3;
    #default-lease-time 600;
    #max-lease-time 7200; 
}
```
- `bashrc` `Aura` <br>
![bashrc_Aura](https://media.discordapp.net/attachments/824131614073683968/1174694611910918277/image.png?ex=6568869c&is=6556119c&hm=e6127fe4977272e59f47d5fa586c09604e693efa7e38bee0f6f6c135c425ca8b&=)

- `terminal` `Aura` <br>
![terminal_Aura](https://media.discordapp.net/attachments/824131614073683968/1174695342793564200/image.png?ex=6568874a&is=6556124a&hm=e4aabcfa8605fa1f8d57a0536b8ba7435cfabe3bdfa898b88b506943c04276bf&=)

- `bashrc` `Heiter` <br>
![bashrc_Heiter](https://media.discordapp.net/attachments/824131614073683968/1174694751908397077/image.png?ex=656886bd&is=655611bd&hm=93beb0c6fcc6b6aaf5b6f7c1832bebd7611914ce5fab5fa5037201d8418e1cdd&=)

- `terminal` `Heiter` <br>
![terminal_Heiter](https://media.discordapp.net/attachments/824131614073683968/1174695739423736010/image.png?ex=656887a9&is=655612a9&hm=c1c50475aa4619ec787550388455fa73cabe0f65b909a657010d63c969d9cd15&=)

- `terminal` `Client` <br>
![terminal_client](https://media.discordapp.net/attachments/824131614073683968/1174696101182447716/image.png?ex=656887ff&is=655612ff&hm=9c1356f9b7d4319c221140d8e90da41e3348cb939afac1962d7a438b5f1d2df3&=)
## Number 5
```
Lama waktu DHCP server meminjamkan alamat IP kepada Client yang melalui Switch3 selama 3 menit sedangkan pada client yang melalui Switch4 selama 12 menit. Dengan waktu maksimal dialokasikan untuk peminjaman alamat IP selama 96 menit (5)
```
- `/etc/dhcp/dhcpd.conf`
```bash
echo subnet 10.62.1.0 netmask 255.255.255.0 {
}

subnet 10.62.4.0 netmask 255.255.255.0 {
    # range 10.62.4.12 10.62.4.20;
    # range 10.62.4.160 10.62.4.168;
    # option routers 10.62.4.1;
    # option broadcast-address 10.62.4.255;
    # option domain-name-servers 10.62.1.3;
    default-lease-time 600;
    max-lease-time 7200;
}

subnet 10.62.3.0 netmask 255.255.255.0 {
    # range 10.62.3.16 10.62.3.32;
    # range 10.62.3.64 10.62.3.80;
    # option routers 10.62.3.1;
    # option broadcast-address 10.62.3.255;
    # option domain-name-servers 10.62.1.3;
    default-lease-time 600;
    max-lease-time 7200; 
}
```

## Number 6
```
Pada masing-masing worker PHP, lakukan konfigurasi virtual host untuk website berikut dengan menggunakan php 7.3. (6)
```
- install lynx di worker maupun client (PHP khusunya)
- `~/scriptVH.sh`
```sh
wget -O '/var/www/granz.channel.i07.com' 'https://drive.google.com/u/0/uc?id=1ViSkRq7SmwZgdK64eRbr5Fm1EGCTPrU1&export=download'
unzip -o /var/www/granz.channel.i07.com -d /var/www/
rm /var/www/granz.channel.i07.com
mv /var/www/modul-3 /var/www/granz.channel.i07.com

cp /etc/nginx/sites-available/default /etc/nginx/sites-available/granz.channel.i07.com
ln -s /etc/nginx/sites-available/granz.channel.i07.com /etc/nginx/sites-enabled/
rm /etc/nginx/sites-enabled/default

echo 'server {
    listen 80;
    server_name _;

    root /var/www/granz.channel.i07.com;
    index index.php index.html index.htm;

    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/run/php/php7.3-fpm.sock;
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
        include fastcgi_params;
    }
}' > /etc/nginx/sites-available/granz.channel.i07.com

service php7.3-fpm start
service nginx restart
```
- `~/.bashrc`
Jangan lupa tambahkan bash yang mengarah ke script diatas `bash ~/scriptVH.sh`
- `terminal`
Di worker jalankan `lynx localhost`, sedangkan di client bisa dijalankan `lynx 10.62.3.1` dimana ip tersebut merupakan ip dari PHP worker

![image](https://github.com/Pascalrjt/Jarkom-Modul-3-I07-2023/assets/89951546/9a8e3f30-064e-4e76-bc69-a7feb98924bf)

## Number 7
```
Kepala suku dari Bredt Region memberikan resource server sebagai berikut:
Lawine, 4GB, 2vCPU, dan 80 GB SSD.
Linie, 2GB, 2vCPU, dan 50 GB SSD.
Lugner 1GB, 1vCPU, dan 25 GB SSD.
aturlah agar Eisen dapat bekerja dengan maksimal, lalu lakukan testing dengan 1000 request dan 100 request/second. (7)
```

- `DNS Server`
```sh
@       IN      A       192.173.2.3     ; IP Load Balancer 
www     IN      CNAME   riegel.canyon.i07.com.
```
```sh
@       IN      A       192.173.2.3     ; IP Load Balancer 
www     IN      CNAME   granz.channel.i07.com.
```
```sh
echo 'options {
      directory "/var/cache/bind";
      forwarders {
              192.168.122.1;
      };
      // dnssec-validation auto;
      allow-query{any;};
      auth-nxdomain no;
      listen-on-v6 { any; };
}; ' >/etc/bind/named.conf.options
```
- `Eisen`
```sh
cp /etc/nginx/sites-available/default /etc/nginx/sites-available/lb_php

echo ' upstream worker {
    server 10.62.3.1;
    server 10.62.3.2;
    server 10.62.3.3;
}

server {
    listen 80;
    server_name granz.channel.i07.com www.granz.channel.i07.com;

    root /var/www/html;

    index index.html index.htm index.nginx-debian.html;

    server_name _;

    location / {
        proxy_pass http://worker;
    }
} ' > /etc/nginx/sites-available/lb_php

ln -s /etc/nginx/sites-available/lb_php /etc/nginx/sites-enabled/
rm /etc/nginx/sites-enabled/default

service nginx restart
```
- delete or command this line on every worker (dhcp)
```sh
echo nameserver 192.168.122.1 > /etc/resolv.conf
```
- run `ab -n 1000 -c 100 http://www.granz.channel.i07.com/ `

![image](https://github.com/Pascalrjt/Jarkom-Modul-3-I07-2023/assets/89951546/9f150009-ecd0-42fe-8dba-121680c2af0d)

## Number 8
```
Karena diminta untuk menuliskan grimoire, buatlah analisis hasil testing dengan 200 request dan 10 request/second masing-masing algoritma Load Balancer dengan ketentuan sebagai berikut:
Nama Algoritma Load Balancer
Report hasil testing pada Apache Benchmark
Grafik request per second untuk masing masing algoritma. 
Analisis (8)
```

-
## Number 9
```
Dengan menggunakan algoritma Round Robin, lakukan testing dengan menggunakan 3 worker, 2 worker, dan 1 worker sebanyak 100 request dengan 10 request/second, kemudian tambahkan grafiknya pada grimoire. (9)
```
## Number 10
```
Selanjutnya coba tambahkan konfigurasi autentikasi di LB dengan dengan kombinasi username: “netics” dan password: “ajkyyy”, dengan yyy merupakan kode kelompok. Terakhir simpan file “htpasswd” nya di /etc/nginx/rahasisakita/ (10)
```
## Number 11
```
Lalu buat untuk setiap request yang mengandung /its akan di proxy passing menuju halaman https://www.its.ac.id. (11) hint: (proxy_pass)
```
## Number 12
```
Selanjutnya LB ini hanya boleh diakses oleh client dengan IP [Prefix IP].3.69, [Prefix IP].3.70, [Prefix IP].4.167, dan [Prefix IP].4.168. (12) hint: (fixed in dulu clinetnya)
```
## Number 13
```
Semua data yang diperlukan, diatur pada Denken dan harus dapat diakses oleh Frieren, Flamme, dan Fern. (13)
```
## Number 14
```
Frieren, Flamme, dan Fern memiliki Riegel Channel sesuai dengan quest guide berikut. Jangan lupa melakukan instalasi PHP8.0 dan Composer (14)
```
## Number 15
```
Riegel Channel memiliki beberapa endpoint yang harus ditesting sebanyak 100 request dengan 10 request/second. Tambahkan response dan hasil testing pada grimoire.
POST /auth/register (15)
```
## Number 16
```
POST /auth/login (16)
```
## Number 17
```
GET /me (17)
```
## Number 18
```
Untuk memastikan ketiganya bekerja sama secara adil untuk mengatur Riegel Channel maka implementasikan Proxy Bind pada Eisen untuk mengaitkan IP dari Frieren, Flamme, dan Fern. (18)
```
## Number 19
```
Untuk meningkatkan performa dari Worker, coba implementasikan PHP-FPM pada Frieren, Flamme, dan Fern. Untuk testing kinerja naikkan 
- pm.max_children
- pm.start_servers
- pm.min_spare_servers
- pm.max_spare_servers
sebanyak tiga percobaan dan lakukan testing sebanyak 100 request dengan 10 request/second kemudian berikan hasil analisisnya pada Grimoire.(19)
```
## Number 20
```
Nampaknya hanya menggunakan PHP-FPM tidak cukup untuk meningkatkan performa dari worker maka implementasikan Least-Conn pada Eisen. Untuk testing kinerja dari worker tersebut dilakukan sebanyak 100 request dengan 10 request/second. (20)
```
