## Jaringan Komputer Sederhana CPT

Ini adalah bagian bagaimana cara membuat jaringan komputer sederhana dengan cisco packet tracer.

## Penjelasan

Penjelasan singkat sebagai pondasi awal bagaimana cara membuat jaringan komputer seperti **subnet mask**, **subnetting**, **network address**, dan **broadcast address**:

### 1. **Subnet Mask**
- **Apa itu?**: Subnet mask adalah angka 32-bit yang digunakan untuk membagi alamat IP menjadi dua bagian: network dan host.
- **Fungsi**: Menentukan bagian mana dari alamat IP yang digunakan untuk network dan bagian mana yang digunakan untuk host.
- **Contoh**: Untuk subnet mask /24, yaitu 255.255.255.0, berarti 24 bit pertama digunakan untuk network, dan sisanya untuk host.

### 2. **Subnetting**
- **Apa itu?**: Proses membagi jaringan IP besar menjadi subnet lebih kecil.
- **Fungsi**: Meningkatkan efisiensi jaringan dengan mengelompokkan alamat IP dan mempermudah manajemen dan keamanan.
- **Contoh**: Dengan subnet mask /24 (255.255.255.0), kita dapat membagi jaringan tersebut menjadi subnet lebih kecil dengan /25 (255.255.255.128), /26 (255.255.255.192), dll.

### 3. **Network Address**
- **Apa itu?**: Alamat yang digunakan untuk mengidentifikasi sebuah subnet.
- **Fungsi**: Untuk mengidentifikasi dan mengarahkan lalu lintas ke jaringan tertentu. Network address biasanya di gunakan pada router, switch, dan perangkat keras jaringan lainnya.

- **Contoh**: Jika subnet adalah 192.168.1.0/24, maka **192.168.1.0** adalah network address. Ini tidak dapat digunakan oleh perangkat di jaringan individu seperti laptop atau smartphone.

### 4. **Broadcast Address**
- **Apa itu?**: Alamat yang digunakan untuk mengirim pesan ke semua perangkat dalam subnet.
- **Fungsi**: Digunakan untuk mengirim data ke semua host dalam jaringan yang sama.
- **Contoh**: Untuk subnet 192.168.1.0/24, **192.168.1.255** adalah broadcast address. Ini digunakan untuk mengirim pesan ke semua perangkat di subnet tersebut.

## 5. **IP Range**
- **Apa itu?**: Rentang alamat IP yang dapat digunakan dalam suatu subnet.
- **Fungsi**: Menunjukkan semua alamat IP yang tersedia untuk perangkat dalam subnet, mulai dari alamat pertama hingga alamat terakhir.
- **Contoh**: IP range adalah rentang alamat IP yang digunakan dalam jaringan. Ini menunjukkan semua alamat IP yang dapat digunakan dalam subnet tertentu, mulai dari alamat pertama (network address + 1) hingga alamat terakhir (broadcast address - 1). Misalnya, untuk subnet 192.168.1.0/24, IP range-nya adalah dari 192.168.1.1 hingga 192.168.1.254.

## CIDR 

CIDR (Classless Inter-Domain Routing) adalah metode pengalamatan dan routing IP yang menghilangkan batasan kelas tradisional (Class A, B, C) dan memungkinkan alokasi alamat IP yang lebih fleksibel dan efisien. CIDR menggunakan notasi slash (misalnya, /24, /16) untuk menunjukkan jumlah bit yang digunakan untuk bagian network dari alamat IP, yang memungkinkan pembagian alamat IP menjadi subnet yang lebih sesuai dengan kebutuhan jaringan.

Daftar CIDR dan subnet mask yang umum beserta jumlah total IP yang tersedia dalam masing-masing subnet:

| **CIDR Notation** | **Subnet Mask**      | **Total IP Addresses** | **Usable IP Addresses** |
|--------------------|-----------------------|-------------------------|--------------------------|
| /8                 | 255.0.0.0             | 16,777,216              | 16,777,214               |
| /16                | 255.255.0.0           | 65,536                  | 65,534                   |
| /24                | 255.255.255.0         | 256                     | 254                      |
| /25                | 255.255.255.128       | 128                     | 126                      |
| /26                | 255.255.255.192       | 64                      | 62                       |
| /27                | 255.255.255.224       | 32                      | 30                       |
| /28                | 255.255.255.240       | 16                      | 14                       |
| /29                | 255.255.255.248       | 8                       | 6                        |
| /30                | 255.255.255.252       | 4                       | 2                        |

### Penjelasan:

- **Total IP Addresses** mencakup semua alamat dalam subnet, termasuk alamat network dan broadcast.
- **Usable IP Addresses** adalah jumlah alamat yang dapat digunakan oleh perangkat dalam subnet, setelah mengurangi alamat network dan broadcast.

## Contoh Perhitungan Dan Soal

Contoh dan soal :

### Soal 1
**Prefix:** /29  
**IP 1:** 192.168.1.10/29  
**IP 2:** 192.168.1.14/29  

**Network Address:** 192.168.1.8  
**Broadcast Address:** 192.168.1.15  
**Usable IP Range:** 192.168.1.9 - 192.168.1.14

**Analisis:** 192.168.1.10 dan 192.168.1.14 berada dalam rentang IP yang sama.  
**Jawaban:** Ya, bisa saling ping.

### Soal 2
**Prefix:** /30  
**IP 1:** 172.16.0.5/30  
**IP 2:** 172.16.0.6/30  

**Network Address:** 172.16.0.4  
**Broadcast Address:** 172.16.0.7  
**Usable IP Range:** 172.16.0.5 - 172.16.0.6

**Analisis:** 172.16.0.5 dan 172.16.0.6 berada dalam rentang IP yang sama.  
**Jawaban:** Ya, bisa saling ping.

### Soal 3
**Prefix:** /28  
**IP 1:** 10.0.0.4/28  
**IP 2:** 10.0.0.10/28  

**Network Address:** 10.0.0.0  
**Broadcast Address:** 10.0.0.15  
**Usable IP Range:** 10.0.0.1 - 10.0.0.14

**Analisis:** 10.0.0.4 dan 10.0.0.10 berada dalam rentang IP yang sama.  
**Jawaban:** Ya, bisa saling ping.

### Soal 4
**Prefix:** /29  
**IP 1:** 10.10.1.1/29  
**IP 2:** 10.10.1.6/29  

**Network Address:** 10.10.1.0  
**Broadcast Address:** 10.10.1.7  
**Usable IP Range:** 10.10.1.1 - 10.10.1.6

**Analisis:** 10.10.1.1 dan 10.10.1.6 berada dalam rentang IP yang sama.  
**Jawaban:** Ya, bisa saling ping.

### Soal 5
**Prefix:** /30  
**IP 1:** 192.168.2.1/30  
**IP 2:** 192.168.2.2/30  

**Network Address:** 192.168.2.0  
**Broadcast Address:** 192.168.2.3  
**Usable IP Range:** 192.168.2.1 - 192.168.2.2

**Analisis:** 192.168.2.1 dan 192.168.2.2 berada dalam rentang IP yang sama.  
**Jawaban:** Ya, bisa saling ping.

**Kesimpulan:**
PC PC tersebut berada dalam subnet yang sama untuk setiap kasus, sehingga mereka dapat saling ping.

## Tutorial

Tutorial bisa di lihat pada <a href="https://gumayuntech.blogspot.com/2024/06/cara-membuat-jaringan-komputer.html">cara membuat jaringan komputer sederhana dengan CPT</a>. Konfigurasi IP menggunakan DHCP pada tutorial tersebut.
