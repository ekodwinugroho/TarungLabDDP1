# Soal Tutorial

## Benny’s Special Super EZ\* Sims Game

<sub><sup>\*agak susah sih</sup></sub>

### Persoalan

Membuat sebuah game yang sangat mirip dengan permainan SIMS®. Dalam game ini terdapat manusia, setiap manusia mempunyai nama yang unik, dan stamina. Setiap manusia dapat melakukan berbagai aktivitas yang akan mengurangi atau menambahkan stamina tersebut. Buat program untuk game tersebut menggunakan Python dan PBO.

### Format Input

- `hidupkan [nama] dengan stamina [stamina]`  
  Sebuah object manusia akan dihidupkan mengambil `[nama]` dan `[stamina]` dari kalimat inputan.

- `[nama1] sapa [nama2]`  
  Kedua object manusia dengan `[nama1]` dan `[nama2]` akan bertambah staminanya
  masing-masing. Manusia dengan `[nama1]` akan bertambah 20 poin stamina. Serta
  Manusia dengan `[nama2]` akan bertambah 10 poin stamina.

- `[nama] makan [nama_makanan] dengan stamina [jumlah_stamina]`  
  Object manusia dengan `[nama]` akan makan `nama_makanan`. Staminanya akan
  bertambah sebanyak `[jumlah_stamina]`.

- `[nama] tidur selama [jam_tidur] jam` 
  Object manusia dengan `[nama]` akan tidur. Staminanya akan bertambah sebanyak
  15 x `[jam_tidur]`.

- `[nama] olahraga selama [jam_olahraga] jam`  
  Object manusia dengan `[nama]` akan berolahraga. Staminanya akan berkurang
  sebanyak 10 x `[jam_olahraga]`.

- `exit`  
  Program akan berakhir dan akan mencetak keseluruhan data dari manusia yang
  ada.

### Format Output

- `hidupkan [nama] dengan stamina [jumlah_stamina]`  
  `[nama]` telah dihidupkan dengan stamina `[jumlah_stamina]`

- `[nama1] sapa [nama2]`  
  `[nama1]` menyapa `[nama2]` dengan senang gembira  
  `[nama1]` mempunyai stamina sebesar `[jumlah_stamina1]`  
  `[nama2]` mempunyai stamina sebesar `[jumlah_stamina2]`

- `[nama] makan [nama_makanan] dengan kalori [jumlah_kalori]`  
  `[nama]` mempunyai stamina sebesar `[jumlah_stamina]`

- `[nama] tidur selama [jam_tidur] jam` 
  `[nama]` tidur selama `[jam_tidur]` jam  
  `[nama]` mempunyai stamina sebesar `[jumlah_stamina]`

- `[nama] olahraga selama [jam_olahraga] jam`  
  `[nama]` olahraga selama `[jam_olahraga]` jam
  `[nama]` mempunyai stamina sebesar jumlah_stamina

- `exit`  
  `[nama1]` mempunyai stamina sebesar `[jumlah_stamina1]`  
  `[nama2]` mempunyai stamina sebesar `[jumlah_stamina2]`  
  ...dan seterusnya

### Template

Tidak diwajibkan menggunakan template tapi disarankan.

```python
class Manusia:
    def __init__(self, nama, stamina):
        # Masukan data manusia!
        
    def sapa(self, manusia_lain):
        # Tambahkan stamina masing-masing manusia
        
    def makan(self, jumlah_kalori):
        # Tambahkan stamina sesuai dengan ketentuan
        
    def tidur(self, jam_tidur):
        # Tambahkan stamina sesuai dengan ketentuan
        
    def olahraga(self, jam_olahraga):
        # Kurangi stamina sesuai dengan ketentuan
        
    def __str__(self):
        # Mengembalikan string sesuai format
        # Digunakan saat ingin mencetak data object

para_manusia = {}
# Dictionary dengan key nama manusia, dan value object manusia

while True:
    perintah = input()
    if perintah.split()[0] == 'exit':
        for nama_manusia in para_manusia:
            print(para_manusia[nama_manusia])
        break
    elif perintah.split()[0] == 'hidupkan':
        nama_manusia = perintah.split()[1]
        stamina = int(perintah.split()[-1])
        manusia = Manusia(nama_manusia, stamina)
        para_manusia[...] = manusia
        ...
    else:
        ...
```

#### Contoh Input

```
hidupkan adli dengan stamina 2400
hidupkan himlan dengan stamina 1200
adli sapa himlan
hidupkan danirama dengan stamina 1999
adli makan katsu dengan kalori 420
danirama tidur selama 2 jam
himlan olahraga selama 5 jam
exit
```

#### Contoh Output

```
adli telah dihidupkan dengan stamina 2400
himlan telah dihidupkan dengan stamina 1200
adli sapa himlan dengan senang gembira
adli mempunyai stamina sebesar 2420
himlan mempunyai stamina sebesar 1210
danirama telah dihidupkan dengan stamina 1999
adli mempunyai stamina sebesar 2840
danirama tidur selama 2 jam
danirama mempunyai stamina sebesar 2029
himlan olahraga selama 5 jam
himlan mempunyai stamina sebesar 1160
adli mempunyai stamina sebesar 2840
himlan mempunyai stamina sebesar 1160
danirama mempunyai stamina sebesar 2029
```

#### Tips dan Trick

- Panggillah method `__str__` saat ingin mencetak data dari manusia.
- Jika bingung dengan template, anda boleh membuat program yang berbeda dengan
  template. Asalkan masih menggunakan konsep BPO.
- Tidak usah mengurutkan statistik pada pencetakan terakhir.
- Kalau tidak mengerti apa yang harus dilakukan, langsung tanyakan!

#### Catatan

- Masing-masing manusia dijamin mempunyai nama yang berbeda.
- Nama manusia hanya akan terdiri dari satu kata.
- Nama manusia yang akan melakukan kegiatan pasti sudah dihidupkan.
- Stamina pada awalnya dijamin adalah bilangan positif.

### Penilaian

- 85% Kebenaran (Program berjalan, kasus uji benar)
- 10% Kerapihan (Penamaan variabel jelas, mudah dibaca)
- 5% Dokumentasi (Comment pada bagian-bagian penting)

*Kami lebih menghargai kodingan anda yang panjang lebar tetapi hasil jerih
payah anda sendiri ketimbang kodingan yang cantik namun hasil orang lain.*

*Percayalah kesempatan anda untuk bisa tetap bertahan dan berjuang di Fasilkom
ditentukan dari usaha dan kerja keras anda sejak sekarang.*

<br>

**Mata Kuliah PBO**

---

Diambil dari `Lab 8 Senin.pdf` (Tutorial Lab 8 DDP1 C -- 6 Oktober 2017)
