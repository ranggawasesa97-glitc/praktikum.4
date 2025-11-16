# praktikum.4
---
## Judul Tugas

## code python (nama_filnya.py)
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

---
## Tampilan Program
