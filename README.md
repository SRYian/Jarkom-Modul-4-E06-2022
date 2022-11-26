# Jarkom-Modul-4-E06-2022

Repositori Jarkom Modul 4 kelompok E06

<details><summary>Anggota kelompok(click to show)</summary>
<p>

### Kelompok E06 :

1. Billy Brianto 5025201080
2. Atha Dzaky Hidayanto 5025201269
3. Naily Khairiya 5025201244
</p>
</details>

## SOAL
Soal shift dikerjakan pada Cisco Packet Tracer dan GNS3 menggunakan metode perhitungan CLASSLESS yang berbeda.
Keterangan: Bila di CPT menggunakan VLSM, maka di GNS3 menggunakan CIDR atau Sebaliknya


## JAWABAN
## VLSM - CPT 
#### Pembagian Subnet
Pertama - tama menentukan subnet dari topologi yang ada. Lingkari setiap host yang terhubung pada interface router dan menghitung IP yang dibutuhkan. 

<img width="606" alt="image" src="https://user-images.githubusercontent.com/72675854/204082120-e8857fff-d3c9-4293-90c5-ad9244a4ff9f.png">

#### Jumlah IP
berikut merupakan jumlah IP yang didapat

<img width="201" alt="image" src="https://user-images.githubusercontent.com/72675854/204082243-bb463df3-3525-4de8-8c53-ada801a9217b.png">

#### VLSM Tree
Dari jumlah IP yang didapat dibuat VLSM tree sebagai berikut

![image](https://user-images.githubusercontent.com/72675854/204082356-19b9a11f-3e92-4710-baba-9730181bea86.png)

Pada tree tersebut diturunkan sesuai netmask diatasnya. Dari /20 ke /21 dan seterusnya sampai semua terpenuhi. Serta pada bagian yang diwarnai merah berarti tidak digunakan. Bagian hijau adalah yang digunakan.

#### Pembagian IP
Dari tree diatas didapatkan pembagian IP sebagai berikut

<img width="483" alt="image" src="https://user-images.githubusercontent.com/72675854/204082459-4db52143-9442-4881-af0c-6c0a58ff35a3.png">

Setelah didapatkan pembagian tersebut maka bisa dilakukann configurasi VLSM pada CPT

#### Config VLSM pada CPT
Menambahkan port pada pada bagian physical

<img width="340" alt="image" src="https://user-images.githubusercontent.com/72675854/204082665-2a908ff0-1556-4836-8ac9-70fd03de84a4.png">

#### Config IP 

<img width="346" alt="image" src="https://user-images.githubusercontent.com/72675854/204082739-1c601fa9-c03f-4e13-a544-9c483d955467.png">

Contoh pada The Order, kita menambahkan IP dan Subnet Mask yang sesuai dengan pembagian yang sudah dilakukan. IP ditambah 1 dari subnetnya. Pastikan bagian port On.

Tambahkan gateway yang mengarah ke router terdekat pada server dan client pada semua node.

<img width="349" alt="image" src="https://user-images.githubusercontent.com/72675854/204082829-5394e092-e386-4e5e-9ec8-e75aedc9e9f9.png">


### Routing

Routing dilakukan pada router. Klik router. Klik tab config menu static dan tambahkan data.

##### The Refonance
192.195.0.4/30 via 192.195.0.10<br>
192.195.0.64/26 via 192.195.0.10<br>
192.195.8.0/22 via 192.195.0.1<br>
192.195.0.0/30 via 192.195.0.10<br>
192.195.2.0/24 via 192.195.0.10<br>
192.195.0.24/30 via 192.195.0.26<br>
192.195.6.0/23 via 192.195.0.26<br>
192.195.0.16/30 via 192.195.0.18<br>
192.195.0.128/30 via 192.195.0.18<br>
192.195.0.20/30 via 192.195.0.18<br>
192.195.1.128/25 via 192.195.0.18<br>
192.195.1.0/25 via 192.195.0.18<br>
192.195.0.12/30 via 192.195.0.18<br>
192.195.4.0/23 via 192.195.0.18<br>
192.195.3.0/24 via 192.195.0.18<br>
192.195.0.28/30 via 192.195.0.18<br>


<img width="343" alt="image" src="https://user-images.githubusercontent.com/72675854/204084276-0251d716-3e3f-41e7-8d42-e41513266d8d.png">




##### The Instrument
0.0.0.0/0 via 192.195.0.17<br>
192.195.0.20/30 via 192.195.0.22<br>
192.195.1.128/25 via 192.195.0.22<br>
192.195.1.0/25 via 192.195.0.22<br>
192.195.0.12/30 via 192.195.0.14<br>
192.195.3.0/24 via 192.195.0.14<br>
192.195.4.0/23 via 192.195.0.14<br>
192.195.0.28/30 via 192.195.0.14<br>

<img width="345" alt="image" src="https://user-images.githubusercontent.com/72675854/204084283-5d480499-f268-4b1c-b8a4-400b692a00d7.png">




##### The Order
0.0.0.0/0 via 192.195.0.9 <br>
192.195.8.0/22 via 192.195.0.6<br>
192.195.0.0/30 via 192.195.0.6<br>
192.195.2.0/24 via 192.195.0.6<br>

<img width="345" alt="image" src="https://user-images.githubusercontent.com/72675854/204084302-26a60893-bd85-4f8f-8001-aec1ca4bd99f.png">




##### The Minister
0.0.0.0/0 via 192.195.0.5<br>
192.195.2.0/24 via 192.195.0.2<br>

<img width="350" alt="image" src="https://user-images.githubusercontent.com/72675854/204084347-1d9f3c8f-7180-4c52-a627-8dc26161dd9b.png">


##### The Firefist
0.0.0.0/0 via 192.195.0.13<br>
192.195.0.28/30 via 192.195.3.3<br>

<img width="347" alt="image" src="https://user-images.githubusercontent.com/72675854/204084355-1e1870e4-dc84-436b-8086-eee5bcd96efa.png">



##### The Daundless
0.0.0.0/0 via 192.195.0.1

<img width="347" alt="image" src="https://user-images.githubusercontent.com/72675854/204084366-6c58ec87-9988-4af0-8b41-faed7cad4560.png">



##### The Magical
0.0.0.0/0 via 192.195.0.25


<img width="349" alt="image" src="https://user-images.githubusercontent.com/72675854/204084335-82326d84-f203-4034-9acd-08bf0caa2ec8.png">



##### The Profound
0.0.0.0/0 via 192.195.0.21

<img width="346" alt="image" src="https://user-images.githubusercontent.com/72675854/204084388-6d1a3545-77e8-4214-b1d8-c59fa6e1cd66.png">



##### The Queen
0.0.0.0/0 via 192.195.3.1

<img width="349" alt="image" src="https://user-images.githubusercontent.com/72675854/204084377-9e763788-0f12-43eb-9ac0-54510f6a7c69.png">

### Testing
<img width="528" alt="image" src="https://user-images.githubusercontent.com/72675854/204084439-679e58eb-bbbd-4fd6-8726-2a46aa269e5b.png">


## CIDR - GNS3

### Penggabungan Subnet


<img width="183" alt="image" src="https://user-images.githubusercontent.com/72675854/204090524-8b688023-8d5b-4fed-940a-b832d937b017.png">

<img width="502" alt="image" src="https://user-images.githubusercontent.com/72675854/204091288-b20652c1-4d2d-4baa-8bab-6623876927c5.png">


<img width="202" alt="image" src="https://user-images.githubusercontent.com/72675854/204090534-b67382f8-1fb6-4de7-8846-9c5fe150ceb3.png">

<img width="453" alt="image" src="https://user-images.githubusercontent.com/72675854/204091309-905835f8-ebb4-47a2-bb73-e01a10a53b67.png">

<img width="195" alt="image" src="https://user-images.githubusercontent.com/72675854/204090541-b3a681e4-24dd-4698-b8c8-91468fed0a10.png">


<img width="456" alt="image" src="https://user-images.githubusercontent.com/72675854/204091318-c7823207-b730-4c74-8077-54306a9d04cc.png">




<img width="183" alt="image" src="https://user-images.githubusercontent.com/72675854/204090548-8b418682-e23c-4ad0-a460-28df0610b86f.png">

![E](https://user-images.githubusercontent.com/72675854/204091329-0d8baa36-01f2-41c2-952a-7981211eab9a.jpg)


<img width="197" alt="image" src="https://user-images.githubusercontent.com/72675854/204090555-ba1e7881-36bb-460c-afe3-108dfad128f6.png">

![F](https://user-images.githubusercontent.com/72675854/204091346-346ef112-c9ff-495d-a8b0-58fef9e65b05.jpg)


<img width="194" alt="image" src="https://user-images.githubusercontent.com/72675854/204090559-ed653aa0-36db-4f42-927f-d02d68efb486.png">


![G1](https://user-images.githubusercontent.com/72675854/204091350-0a249640-5837-49eb-813a-2d3a2af66d18.jpg)


<img width="481" alt="image" src="https://user-images.githubusercontent.com/72675854/204090569-7a006767-6e79-44fb-82a5-ea3ecc95a697.png">

![H](https://user-images.githubusercontent.com/72675854/204091354-61768854-fa57-4266-acdc-ad9b17df98c1.jpg)

### CIDR Tree

![image](https://user-images.githubusercontent.com/72675854/204090248-9d5d42fb-ec03-4d12-b890-2ef2dd220a7a.png)

### Configuration
### Routing
### Testing





