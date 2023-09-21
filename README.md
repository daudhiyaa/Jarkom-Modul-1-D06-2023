# <div align="center"><p>Jarkom-Modul-1-D06-2023</p></div>

## Anggota Kelompok

| Nama                               | NRP        |
| ---------------------------------- | ---------- |
| Achmad Khosyi’ Assajjad Ramandanta | 5025211007 |
| Daud Dhiya' Rozaan                 | 5025211021 |

## No 1
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.
- Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? 
- Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 
- Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
- Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

**Jawab**

Untuk mencari packet yang memiliki fungsi mengunggah file, kita dapat melakukan filter di wireshark dengan command `ftp.request.command == "STOR"`.

Lalu pencet packet tersebut dan buka bagian `Transmission Control Protocol`. Disana akan terlihat berapa sequence number (raw) dan acknowledge number (raw) dari packet tersebut.

`Foto SS`

- **Jawaban nomor 1a : 258040667**
- **Jawaban nomor 1b : 1044861039**

Untuk mencari packet yang menerima respon dari packet yang telah mengunggah file tersebut, maka cukup scroll kebawah dan biasanya 2 packet dibawah packet yang mengunggah adalah packet yang menerima respon. Karena nomor packet yang mengunggah adalah 147, maka packet nomor packet yang menerima respon adalah 149.

Sama seperti sebelumnya, tinggal pencet packet tersebut dan buka bagian `Transmission Control Protocol`. Disana akan terlihat berapa sequence number (raw) dan acknowledge number (raw) dari packet tersebut.

`Foto SS`

- **Jawaban nomor 1c : 1044861039**
- **Jawaban nomor 1d : 258040696**

`Foto SS Flag`?

## No 2

## No 3

## No 4

## No 5
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.
- Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
- Port berapakah pada server yang digunakan untuk service SMTP?
- Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

**Jawab**
Pertama-tama, karena pada nomor 5 ini kami dikasih 2 file yaitu file soal5.pcap dan file zippppfileee.zip, dan kami harus mencari password untuk membuka file .zip tersebut terlebih dahulu agar kita mendapatkan `nc` agar bisa menjawab pertanyaan.

Karena pada nomor 5 topiknya adalah `SMTP`, maka kami berusaha untuk mencari packet yang relevan dengan `MAIL`. Ditemukan satu packet dengan isi info `MAIL`, lalu klik kanan pada packet tersebut dan klik `follow TCP Stream`.

`Foto SS`

Di dalam file tersebut, ditemukan password untuk membuka file .zip-nya yaitu `NWltcGxlUGFzNXdvcmQ=` namun harus di decode menggunakan `Base64` terlebih dahulu.

`Foto SS`

Lalu, kami melakukan decode di web `base64decode.org` dan menemukan password asli dari file .zip-nya yaitu `5implePas5word`.

`Foto SS`

Lalu, tinggal extract file .zip tersebut dan kami mendapatkan file .txt yang isinya terdapat `nc` untuk menjawab pertanyaan.

`Foto SS`

Untuk menjawab nomor 5a, tinggal buka file `soal5.pcap`, lalu scroll kebawah dan lihat nomor packet terakhir.

`Jawaban 5a : 60`

Untuk menjawab nomor 6b, tinggal menggunakan filter `smtp`, lalu klik pada salah satu packet agar dapat mengetahui port dari `smtp`. 

`Jawaban 5b : 25`

Untuk menjawab nomor 6c, kami mencari ip yang infonya berhubungan dengan komunikasi secara global, salah satunya adalah komunikasi email. Dan ditemukan antara `10.10.1.4` atau `74.53.140.154`. Karena kami menganggap bahwa ip dengan awalan `10` adalah ip dari ITS, maka kami menjawab ip dengan awalan `74`.

`Jawaban 5c : 74.53.140.154`

`Foto SS Flag`?

## No 6

## No 7

## No 8

## No 9

## No 10
