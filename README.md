# praktikum.4
---
## Manajemen Nilai Mahasiswa Sederhana (List & Loop)
Kodingan ini bertujuan untuk membuat aplikasi konsol sederhana menggunakan Python yang berfungsi sebagai alat Manajemen Data dan Nilai Akademik Mahasiswa.
---
## flowchart 
<img width="261" height="921" alt="index" src="https://github.com/user-attachments/assets/2bab64be-9f2e-48bb-b4ca-7cc929d66043" />

## penjelasan flowchart

---
## code python (data_mahasiswa.py)
```python
data_mahasiswa = []

print("=== PROGRAM MANAJEMEN NILAI MAHASISWA (LIST & LOOP) ===")

while True:
    print("\n--- Input Data Mahasiswa ---")
    
    try:
        nama = input("Nama: ")
        nim = input("NIM: ")
        
        nilai_tugas = int(input("Nilai Tugas: "))
        nilai_uts = int(input("Nilai UTS: "))
        nilai_uas = int(input("Nilai UAS: "))

        nilai_akhir = (nilai_tugas * 0.30) + (nilai_uts * 0.35) + (nilai_uas * 0.35)
        
        nilai_akhir_bulat = round(nilai_akhir)
        
        data_mahasiswa.append([nama, nim, nilai_tugas, nilai_uts, nilai_uas, nilai_akhir_bulat])
        
    except ValueError:
        print("Input nilai harus berupa angka. Silakan coba lagi.")
        continue 

    
    tambah_lagi = input("\nTambah data (y/t)? ").lower()
    if tambah_lagi == 't': 
        break 


if not data_mahasiswa:
    print("\nTidak ada data mahasiswa untuk ditampilkan.")
else:
    print("\n" + "="*70)
    print(" " * 20 + "DAFTAR NILAI MAHASISWA")
    print("="*70)
    
    print(f"| {'No':<3} | {'Nama':<15} | {'NIM':<10} | {'Tugas':<6} | {'UTS':<5} | {'UAS':<5} | {'Akhir':<7} |")
    print("-" * 70)

    no = 1
    for mhs in data_mahasiswa:
        
        
        print(f"| {no:<3} | {mhs[0]:<15} | {mhs[1]:<10} | {mhs[2]:<6d} | {mhs[3]:<5d} | {mhs[4]:<5d} | {mhs[5]:<7.2f} |")
        no += 1
    
    print("="*70)
```
## penjelasan code
- ```data_mahasiswa = []``` List utama diinisialisasi untuk menampung semua data.
- ```while True:```	Memulai perulangan tak terbatas yang akan meminta input data mahasiswa baru.
- ```nilai_tugas = int(input(...))```	Meminta input nilai dan menyimpannya sebagai bilangan bulat (int).
- ```nilai_akhir = (...)```	Menghitung Nilai Akhir menggunakan rumus rata-rata tertimbang dan menyimpannya.
- ```data_mahasiswa.append([...])```	Menambahkan data mahasiswa (berupa List lain) ke List utama (data_mahasiswa).
- ```if tambah_lagi == 't': break``` 	Menghentikan perulangan jika pengguna memasukkan 't'.
- ```for mhs in data_mahasiswa:```	Memulai perulangan untuk mencetak setiap data yang sudah tersimpan.
- ```{mhs[0]:<15}```	Mencetak nilai dari List (mhs[0], yaitu Nama) dan mengaturnya rata kiri (<) dengan lebar 15 karakter (15) agar tabel lurus.

Program ini punya resep khusus untuk menentukan Nilai Akhir:
1. Nilai Tugas dianggap paling ringan, hanya menyumbang 30% (atau 0.30) dari total nilai.
2. Nilai UTS (Ujian Tengah Semester) dianggap lebih penting, menyumbang 35% (atau 0.35).
3. Nilai UAS (Ujian Akhir Semester) juga menyumbang 35% (atau 0.35).

Proses Perhitungannya di KodeDi dalam kode, yang terjadi adalah: 
1. Program mengambil nilai Tugas, UTS, dan UAS yang Anda masukkan.
2. Setiap nilai dikalikan dengan bobotnya. Misalnya, jika Nilai Tugas Anda 70, maka kontribusinya adalah $70 \times 0.30 = 21$.
3. Ketiga hasil perkalian itu dijumlahkan.
4. Hasil penjumlahan tersebut adalah Nilai Akhir mentah (misalnya, 71.75).
5. Terakhir, program menggunakan perintah round(..., 2) untuk memastikan nilai tersebut dibulatkan rapi menjadi dua angka di belakang koma (misalnya, tetap 71.75), sebelum disimpan ke dalam daftar data.

Jadi, Hasil Akhir adalah hasil terpenting dari seluruh proses input, karena merupakan nilai yang ditaruh di kolom terakhir daftar nilai mahasiswa.

Saat program mencetak tabel, ia menggunakan kode format khusus: {mhs[5]:<7.2f}.
- mhs[5] adalah cara program mengambil Nilai Akhir dari daftar data.
- <7.2f adalah aturannya:
    - <7 memastikan ada ruang 7 karakter di layar (lebar kolom).
    - .2f adalah perintah untuk memastikan nilai ini selalu terlihat dengan dua angka desimal (seperti 71.75 atau 80.00).
---
## Tampilan Program
<img width="1918" height="854" alt="image" src=image.png />
