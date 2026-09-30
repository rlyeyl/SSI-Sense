# SSI-Sense
**Sistem Diagnosis Infeksi Pasca Operasi berbasis Knowledge-Based System & Forward Chaining**

SSI-Sense adalah prototipe *knowledge-based system* (KBS) untuk mengklasifikasikan Surgical Site Infection (SSI) — infeksi pasca operasi — menjadi tiga kategori NHSN: **superficial incisional**, **deep incisional**, dan **organ/space**. Basis pengetahuannya disederhanakan dari pedoman [NHSN Chapter 9: Surgical Site Infection (SSI) Event](https://www.cdc.gov/nhsn/pdfs/pscmanual/9pscssicurrent.pdf) (CDC, Jan. 2026), dievaluasi dengan pendekatan *forward chaining*: kedalaman jaringan (`Kulit_Subkutan`, `Jaringan_Lunak_Otot`, `Organ_Rongga`) bersifat kumulatif dan melekat pada 9 prosedur demonstrasi, sehingga temuan klinis yang dimasukkan pengguna dievaluasi terhadap level yang relevan tanpa perlu memilih kedalaman secara manual.

Proyek ini dikembangkan sebagai sarana pembelajaran penerapan representasi pengetahuan dan inferensi otomatis, **bukan** alat diagnosis klinis maupun dasar pengambilan keputusan medis.

## Fitur

- **Form pemeriksaan** — pilih salah satu dari 9 prosedur demo, isi tanggal operasi/temuan, temuan klinis (drainase, insisi dibuka, abses, drain organ/space), terapi antimikroba, dan gejala penyerta. Klasifikasi diperbarui otomatis setiap input berubah.
- **Jejak penalaran** — panel yang bisa dibuka/tutup, menampilkan tiap fakta dan predikat turunan (`Tanggal_Valid_30`, `Terapi_Valid`, `Gejala_Deep`, dst.) beserta nilai benar/salahnya.
- **Manajemen data pasien simulasi** — simpan kasus dengan kode pasien lewat tombol *Save data* (tersimpan di `localStorage` browser, bertahan lintas sesi selama browser/perangkat yang sama), muat ulang, atau hapus lewat daftar pasien.
- **4 contoh pasien siap pakai**, satu untuk tiap hasil klasifikasi (superficial, deep, organ/space, dan satu kasus deep lain dengan jalur insisi dibuka + terapi).
  
