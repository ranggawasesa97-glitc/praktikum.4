```python
# 1. Buat sebuah list sebanyak 5 elemen dengan nilai bebas (List A)
A = [10, 'apel', 3.14, 'pisang', 50]
print(f"List A awal: {A}")
# Output: List A awal: [10, 'apel', 3.14, 'pisang', 50]

print("\n--- A. Akses List ---")
# Akses List A: Indeks dimulai dari 0.

# 1. Tampilkan elemen ke-3 (Indeks 2)
print(f"1. Elemen ke-3: {A[2]}") 
# Output: 3.14

# 2. Ambil nilai elemen ke-2 sampai elemen ke-4 (Indeks 1 sampai Indeks 3)
print(f"2. Elemen ke-2 sampai ke-4: {A[1:4]}")
# Output: ['apel', 3.14, 'pisang']

# 3. Ambil elemen terakhir (Indeks -1)
print(f"3. Elemen terakhir: {A[-1]}") 
# Output: 50

print("\n--- B. Ubah Elemen List ---")

# 1. Ubah elemen ke-4 dengan nilai lainnya (Indeks 3)
A[3] = 'mangga'
print(f"1. Setelah ubah elemen ke-4: {A}") 
# Output: [10, 'apel', 3.14, 'mangga', 50]

# 2. Ubah elemen ke-4 sampai dengan elemen terakhir (Indeks 3 sampai akhir)
A[3:] = ['jeruk', 99]
print(f"2. Setelah ubah elemen ke-4 sampai terakhir: {A}")
# Output: [10, 'apel', 3.14, 'jeruk', 99]

print("\n--- C. Tambah Elemen List ---")

# 1. Ambil 2 bagian dari list pertama (A) dan jadikan list ke-2 (B)
# Mengambil Indeks 0 dan 1 dari List A
B = A[0:2] 
print(f"1. List B (hasil slicing A): {B}") 
# Output: [10, 'apel']

# 2. Tambah list B dengan nilai string
B.append("anggur")
print(f"2. List B setelah append string: {B}") 
# Output: [10, 'apel', 'anggur']

# 3. Tambah list B dengan 3 nilai
B.extend([1, 2, 3])
print(f"3. List B setelah extend 3 nilai: {B}") 
# Output: [10, 'apel', 'anggur', 1, 2, 3]

# 4. Gabungkan list B dengan list A
C = B + A
print(f"4. List C (gabungan B + A): {C}") 
# Output: [10, 'apel', 'anggur', 1, 2, 3, 10, 'apel', 3.14, 'jeruk', 99]
```
