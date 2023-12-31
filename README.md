# Jarkom-Modul-4-B14-2023

## Pendahuluan

Repository ini dibentuk untuk menyelesaikan tugas praktikum Jaringan Komputer.

Anggota Kelompok B14:
| Nama | NRP |
| :---: | :---: |
| Muhammad Arkan Karindra Darvesh | 5025211236 |

## Pembahasan

### Soal
1. Soal shift dikerjakan pada Cisco Packet Tracer dan GNS3 menggunakan metode perhitungan CLASSLESS yang berbeda.
2. Keterangan: Bila di CPT menggunakan VLSM, maka di GNS3 menggunakan CIDR atau sebaliknya
3. Jika tidak ada pemberitahuan revisi soal dari asisten, berarti semua soal BERSIFAT BENAR dan DAPAT DIKERJAKAN.
4. Untuk di GNS3 CLOUD merupakan NAT1 jangan sampai salah agar bisa terkoneksi internet.
5. Pembagian IP menggunakan Prefix IP yang telah ditentukan pada modul pengenalan
6. Pembagian IP dan routing harus SE-EFISIEN MUNGKIN.
7. Gambar topologi yang lebih jelas dapat diakses pada <a href="https://drive.google.com/file/d/1VmJXOyEoWru1tfXISOgoJiPfE1hpbptM/view?usp=sharing">link berikut</a>



Hal yang perlu diperhatikan

1. Gunakan prefix IP sesuai dengan prefix IP masing-masing.
2. Terdapat template spreadsheet untuk mempermudah penilaian, gunakan template tersebut untuk melakukan penghitungan subnetting.
3. Hasil perhitungan subnetting dan pohon pembagian IP serta file .pkt di submit pada link di atas.
4. File yang didemokan adalah file .pkt yang telah disubmi5t
5. Pengurangan nilai akan dilakukan ketika:
   
   a. Melanggar salah satu dari tulisan diatas.

   b. Tidak menggunakan PREFIX ip yang ditetapkan sebelumnya

   c. Hasil perhitungan untuk VLSM / CIDR, berbeda dengan di CPT / GNS3

   d. Pembagian IP kurang efisien

   e. Routing kurang efisien

   f. Tidak bisa menjelaskan cara perhitungan VLSM dan CIDR


### Jawaban

Pertama, kita perlu membuat rute subnet untuk topologi yang telah diberikan.
Untuk itu, kita bisa membagina menjadi seperti berikut:


#### [Pembagian IP] VLSM - GNS3
1. VLSM (Variable Length Subnet Masking)

_Variable Length Subnet Masking_ (VLSM) adalah sebuah metode pengalamatan IP yang memungkinkan pengguna untuk menggunakan subnet mask dengan panjang yang bervariasi untuk mengoptimalkan penggunaan alamat IP dalam jaringan. VLSM memungkinkan kita untuk membagi alamat IP secara lebih efisien dengan mengalokasikan blok alamat yang lebih besar untuk subnet yang membutuhkan lebih banyak host dan blok alamat yang lebih kecil untuk subnet yang membutuhkan lebih sedikit host.

Jadi, pada teknik VLSM, subnet mask (netmask) akan diberikan sesuai dengan kebutuhan jumlah alamat IP dari subnet tersebut. Sesuai dengan jumlah alamat ip yang telah kita bagikan.

Langkah 1 - Tentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet dan lakukan labelling netmask berdasarkan jumlah IP yang dibutuhkan.


Nama Subnet	Rute	Jumlah IP	Netmask

A1	Fern-Switch4-AppetitRegion-Switch4-LaubHills	1022	/21

A2	Flamme-Switch5-RohrRoad	1001	/22

A3	Himmel-Switch6-SchweMountains	6	/29

A4	Fern-Flamme	2	/30

A5	Flamme-Himmel	2	/30

A6	Flamme-Frieren	2	/30

A7	Frieren-Switch3-LakeKorridor	25	/27

A8	Frieren-Aura	2	/30

A9	Aura-Eisen	2	/30

A10	Eisen-Switch 1-Revolte-Switch1-Richter	3	/29

A11	Eisen-Linie	2	/30

A12	Linie-Lawine	2	/30

A13	Lawine-Switch7-BredtRegion-Switch7-Heiter	31	/26

A14	Heiter-Switch8-Sein-RiegelCanyon	512	/22

A15	Linie-Switch11-GranzChannel	255	/23

A16	Eisen-Lugner	2	/30

A17	Lugner-Switch9-GrobeForest	251	/24

A18	Lugner-Switch10-TurkRegion	1001	/22

A19	Eisen-Switch0-Stark	2	/30

A20	Aura-Denken	2	/30

A21	Denkern-Switch2-RoyalCapital-Switch2-WilleReg	127	/24
Total		4254	/19

Pembagian IP VLSM

<img width="537" alt="pembagian-ipvlsm" src="https://github.com/Arkandrvesh/Jarkom-Modul-4-B14-2023/assets/116497822/aa32f11d-e055-48cb-8720-9323c9a46c6e">


Tree VLSM

<img width="898" alt="vlsm-revisiTree" src="https://github.com/Arkandrvesh/Jarkom-Modul-4-B14-2023/assets/116497822/0d427866-5037-46cf-a841-2cff3c4741ae">

<img width="917" alt="vlsm-revisiTree2" src="https://github.com/Arkandrvesh/Jarkom-Modul-4-B14-2023/assets/116497822/8585c7ab-148b-4ee7-a510-fd40efc4feac">


Perhitungan VLSM

<img width="382" alt="hitung-vlsm" src="https://github.com/Arkandrvesh/Jarkom-Modul-4-B14-2023/assets/116497822/6a022404-eb53-4a45-b5ac-444d66057aa0">

2. CIDR (Classless Inter Domain Routing)

Classless Inter-Domain Routing merupakan sebuah metode pengalokasian alamat IP dan perutean IP. Internet Engineering Task Force memperkenalkan CIDR pada tahun 1993 untuk mengganti arsitektur pengalamatan dari desain jaringan kelas di internet.

Pembagian IP CIDR

<img width="330" alt="pembagian-ipcidr" src="https://github.com/Arkandrvesh/Jarkom-Modul-4-B14-2023/assets/116497822/dff1e897-74b9-4591-bba6-b8a0905164c3">


Penggabungan CIDR

<img width="388" alt="penggabungan-cidr" src="https://github.com/Arkandrvesh/Jarkom-Modul-4-B14-2023/assets/116497822/96281824-bfee-4481-8aa8-7485c53d0c74">

<img width="385" alt="penggabungan-cidr2" src="https://github.com/Arkandrvesh/Jarkom-Modul-4-B14-2023/assets/116497822/4a4304a1-5273-4297-98ff-2dfd66244829">
<img width="382" alt="penggabungan-cidr3" src="https://github.com/Arkandrvesh/Jarkom-Modul-4-B14-2023/assets/116497822/65677012-1d28-43f4-903e-7289c39d8a78">


Foto topologi penggabungan

![tempsnip - Copy (8) - Copy - Copy](https://github.com/Arkandrvesh/Jarkom-Modul-4-B14-2023/assets/116497822/e6d20299-6f11-436a-87d4-d30a6dd9b455)


Tree CIDR

<img width="319" alt="CIDR_revisi" src="https://github.com/Arkandrvesh/Jarkom-Modul-4-B14-2023/assets/116497822/d9a936b6-c9c8-4945-8c4b-f2cc9c7d8d64">



