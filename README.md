def hitung_nilai_akhir(tugas, uts, uas):
    return 0.3 * tugas + 0.35 * uts + 0.35 * uas

data_mahasiswa = []

while True:
    nama = input("Masukkan nama mahasiswa: ")
    tugas = float(input("Masukkan nilai tugas: "))
    uts = float(input("Masukkan nilai UTS: "))
    uas = float(input("Masukkan nilai UAS: "))
    
    nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
    data_mahasiswa.append({
        'nama': nama,
        'tugas': tugas,
        'uts': uts,
        'uas': uas,
        'nilai_akhir': nilai_akhir
    })
    
    tambah_data = input("Apakah Anda ingin menambah data lagi? (y/t): ").lower()
    if tambah_data == 't':
        break

print("\nDaftar Data Mahasiswa:")
for mahasiswa in data_mahasiswa:
    print(f"Nama: {mahasiswa['nama']}, Tugas: {mahasiswa['tugas']}, UTS: {mahasiswa['uts']}, UAS: {mahasiswa['uas']}, Nilai Akhir: {mahasiswa['nilai_akhir']:.2f}")

![Screenshot 2024-11-22 201310](https://github.com/user-attachments/assets/a2e6356a-b9d8-4f7f-bea4-5812510fd9f7)

Program Mengelola Data Mahasiswa
Deskripsi
Program ini memungkinkan pengguna untuk menambahkan data mahasiswa secara berulang kali dan menghitung nilai akhir berdasarkan nilai tugas, UTS, dan UAS. Program akan menampilkan daftar data mahasiswa setelah pengguna memutuskan untuk berhenti menambah data.

Flowchart

+----------------------------------------------------------+
| Mulai                                                     |
+----------------------------------------------------------+
          |
          v
+-------------------+                      +----------------------+
| Buat list kosong  |                      | Menginput nama       |
| data_mahasiswa    |                      | mahasiswa            |
+-------------------+                      +----------------------+
          |                                            |
          v                                            v
+-------------------+                      +----------------------+
| Meminta input     |                      | Menginput nilai      |
| dari pengguna:    +----------------------> tugas, UTS, UAS     |
| Nama, Tugas, UTS, |                      +----------------------+
| dan UAS           |                                      |
+-------------------+                                      v
          |                                 +------------------------------+
          v                                 | Hitung nilai akhir           |
+-------------------+                      +-------------------------------+
| Hitung nilai      +--------------------->| Nilai Akhir = 0.3*Tugas +     |
| akhir             |                      | 0.35*UTS + 0.35*UAS           |
|                   |                      +-------------------------------+
          |                                           |
          v                                           v
+-------------------+                      +-------------------------------+
| Tambahkan data ke |                      | Tambah data lagi?             |
| list              +--------------------->| (y/t)?                        |
| data_mahasiswa    |                      +-------------------------------+
+-------------------+                                      |
          |                                                |
          v                                                v
+-------------------+                      +-------------------------------+
| Apakah menambah   +--------------------->| Jika 't', tampilkan daftar    |
| data lagi (y/t)?  |                      | data mahasiswa                |
| Ya (y)/Tidak (t)? |                      +-------------------------------+
+-------------------+
          |
          v
+-------------------+
| Tampilkan daftar  |
| data mahasiswa    |
+-------------------+
          |
          v
+----------------------------------------------------------+
| Selesai                                                  |
+----------------------------------------------------------+
