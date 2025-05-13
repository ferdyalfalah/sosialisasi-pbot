# sosialisasi-pbot

# 🌟 Materi Sosialisasi: Pengenalan Coding, Python, dan Teori Probabilitas

## 🧩 SESI 1: Pengenalan Coding

### Apa itu Coding?
- **Coding** = memberi **instruksi kepada komputer** agar melakukan sesuatu.
- Seperti memberi perintah ke robot: "ambil gelas", "nyalakan lampu", dsb.
- Tanpa coding, komputer tidak tahu harus melakukan apa.

### Kenapa Harus Belajar Coding?
- Dunia saat ini sangat bergantung pada teknologi.
- Banyak hal di sekitar kita dibuat dengan coding: **aplikasi, game, IoT, robot, website, AI**, dll.
- **Coding** melatih kita untuk berpikir logis, kreatif, dan menyelesaikan masalah.

### Jenis Bahasa Pemrograman Populer

| Bahasa     | Kegunaan utama                        |
|------------|----------------------------------------|
| **Python** | Mudah, cocok untuk pemula, AI, IoT     |
| **JavaScript** | Website interaktif                     |
| **C/C++**      | Robotika, IoT, performa tinggi         |
| **Java**       | Aplikasi Android                       |

### Coding dalam Dunia IoT
- **Coding** digunakan untuk **mengontrol alat IoT** seperti sensor suhu, smart lamp, atau sistem penyiram otomatis.
- Tanpa coding, alat tidak bisa "berpikir" sendiri.

---

## 💻 SESI 2: Persiapan Coding Python

### Perangkat yang Digunakan
- **Laptop/PC** → ideal
- **HP Android** → bisa gunakan aplikasi: [Pydroid 3](https://play.google.com/store/apps/details?id=ru.iiec.pydroid3)

### Tempat Coding Python
1. **Online** (tanpa instalasi):
   - [Google Colab](https://colab.research.google.com) ✅ disarankan
2. **Offline** (harus instal Python):
   - Python IDLE
   - VS Code + ekstensi Python
   - Jupyter Notebook

### Coba Menjalankan Kode Pertama
```python
print("Halo, Dunia!")
```
Output
```
Halo, Dunia!
```

---

## 🐍 Sesi 3: Dasar-Dasar Python

### ✏️ Komentar & Indentasi
```python
# Ini adalah komentar
if True:
    print("Baris ini memiliki indentasi")
```

---

### 🧮 Variabel & Tipe Data

```python
nama = "Budi"        # string
umur = 17            # integer
tinggi = 1.65        # float
aktif = True         # boolean
```

---

### 📦 Struktur Data: List (Array)
```python
angka = [10, 20, 30]
print(angka[0])  # Output: 10
```

---

### ➗ Operator Matematika
```python
a = 10
b = 3

print(a + b)  # Penjumlahan
print(a - b)  # Pengurangan
print(a * b)  # Perkalian
print(a / b)  # Pembagian
print(a % b)  # Sisa bagi (modulus)
print(a ** b) # Pangkat
```

---

### ⚖️ Operator Perbandingan & Logika
```python
print(a == b)  # Sama dengan
print(a != b)  # Tidak sama

x = True
y = False
print(x and y)  # AND
print(x or y)   # OR
```

---

### 🧑‍💻 Input dari Pengguna
```python
nama = input("Siapa namamu? ")
umur = int(input("Berapa umurmu? "))
```

---

### 🔁 Percabangan dan Perulangan
```python
if umur >= 17:
    print("Dewasa")
else:
    print("Anak-anak")
```

```python
for i in range(3):
    print("Perulangan ke-", i)
```

---

### 🧱 Fungsi
```python
def sapa(nama):
    print("Halo", nama)

sapa("Dina")
```

---

### 🧰 Import Library
```python
import random
import math

print(random.randint(1, 10))  # Angka acak
print(math.sqrt(16))          # Akar kuadrat
```

---

## 🎲 Sesi 4: Teori Probabilitas Dasar + Python

### 🎯 Apa itu Probabilitas?
> Probabilitas adalah peluang terjadinya suatu peristiwa. Nilai berada antara 0 (mustahil) dan 1 (pasti).

Contoh:
- Peluang muncul angka 6 pada dadu = `1/6 ≈ 0.166`

---

### 🧪 Simulasi Lempar Koin
```python
import random
hasil = random.choice(["Head", "Tail"])
print("Hasil lemparan:", hasil)
```

---

### 🎲 Simulasi 100 Kali Lempar Dadu
```python
jumlah = 100
angka_6 = 0

for i in range(jumlah):
    hasil = random.randint(1, 6)
    if hasil == 6:
        angka_6 += 1

peluang = angka_6 / jumlah
print("Peluang muncul angka 6:", peluang)
```

---

## 🎁 Sesi 5: Studi Kasus
### 📜 Program Simulasi Diskon Berdasarkan Probabilitas

```python
# Meminta data pelanggan
name = input("Enter customer name: ")
dob = int(input("Enter date of birth (number only): "))
month = input("Enter month of birth: ")

# Menyimpan data ke dalam dictionary
customer = {
    "name": name,
    "date_of_birth": dob,
    "month_of_birth": month
}

# Menentukan status berdasarkan tanggal lahir
if dob % 2 == 0:
    customer["status"] = "even customer"
else:
    customer["status"] = "odd customer"

# Menampilkan data customer yang telah diperbarui
print("\nUpdated customer data:")
print(customer)

# Menghasilkan angka acak antara 1 sampai 4
import random
random_number = random.randint(1, 4)
print(f"\nRandom number generated: {random_number}")

# Menentukan dan menambahkan diskon berdasarkan kesesuaian status dan angka acak
if random_number % 2 == 0 and customer["status"] == "even customer":
    customer["discount"] = "30%"
    print("Congratulations! You're an even customer and got a lucky even number. You get a 30% discount!")
elif random_number % 2 != 0 and customer["status"] == "odd customer":
    customer["discount"] = "30%"
    print("Congratulations! You're an odd customer and got a lucky odd number. You get a 30% discount!")
else:
    customer["discount"] = "0%"
    print("Sorry, no matching luck today. You get 0% discount.")

# Menampilkan data akhir
print("\nFinal customer data:")
print(customer)
```

---

### 💡 Penjelasan:
- Program menggunakan **input data pelanggan**.
- Menghitung **status pelanggan** dari tanggal lahir (genap/ganjil).
- Menghasilkan **angka acak** sebagai bentuk probabilitas.
- Jika angka acak dan status cocok → dapat **diskon 30%**.
- Jika tidak cocok → **tidak dapat diskon**.

---

### 🧠 Konsep yang Diterapkan:
- Tipe data: string, integer, dictionary
- Kondisional: `if`, `else`
- Random: `random.randint()`
- Operator modulus: `%` untuk menentukan genap/ganjil
- Simulasi probabilitas berdasarkan kecocokan dua kondisi

---

