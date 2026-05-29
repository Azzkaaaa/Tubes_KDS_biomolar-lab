# BioMolar Lab

BioMolar Lab adalah proyek analisis molaritas dan osmolaritas larutan biologis. Proyek ini menggunakan data sampel plasma untuk menghitung osmolaritas dengan metode Dorwart-Chalmers dan Van't Hoff extended, mendeteksi status osmolaritas, mengidentifikasi indikasi kondisi klinis, serta membuat visualisasi hasil analisis.

## Fitur Singkat

- Menghitung osmolaritas plasma dari data ion utama, glukosa, dan BUN.
- Membandingkan metode Dorwart-Chalmers dengan Van't Hoff extended.
- Mengklasifikasikan sampel menjadi hipoosmolar, normal, atau hiperosmolar.
- Mendeteksi kondisi klinis seperti hipernatremia, hiponatremia, hiperglikemia, azotemia, asidosis, dan alkalosis metabolik.
- Menghasilkan file hasil analisis dan grafik pada folder `output/`.
- Menyediakan GUI simulator osmosis sel darah merah berbasis Tkinter.

## Struktur Proyek

```text
.
|-- data/                 # Dataset sampel plasma dan rentang referensi ion
|-- docs/                 # Dokumen laporan
|-- output/               # Hasil analisis dan visualisasi
|-- src/                  # Source code utama
|   |-- main.py           # Entry point analisis dataset
|   |-- gui.py            # GUI simulator osmosis
|   |-- modules/          # Modul molaritas, osmolaritas, klasifikasi, visualisasi
|   `-- utils/            # Loader, converter, dan validator
|-- tests/                # Unit test
|-- notebook.ipynb        # Notebook eksplorasi/analisis
|-- requirements.txt      # Daftar dependency
`-- README.md
```

## Cara Run

Pastikan Python sudah terinstall. Disarankan menggunakan virtual environment.

### 1. Buat dan aktifkan virtual environment

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 2. Install dependency

```powershell
pip install -r requirements.txt
```

### 3. Jalankan analisis utama

```powershell
python -m src.main
```

Output analisis akan muncul di terminal dan file hasil akan disimpan pada folder `output/`, termasuk:

- `hasil_analisis.csv`
- `perbandingan_metode.png`
- `osmolal_gap.png`
- grafik kontribusi ion per sampel

### 4. Jalankan GUI simulator

```powershell
python -m src.gui
```

GUI ini digunakan untuk mensimulasikan perubahan sel darah merah pada larutan hipotonik, isotonik, dan hipertonik.

### 5. Jalankan unit test

```powershell
pytest
```

## Pembagian Tugas

| Anggota | Tugas |
| --- | --- | 
| 13523137 | Perancangan arsitektur repo dan utils |
| 13523162 | Implementasi module molaritas dan klasifikasi | 
| 13523163 | Implementasi GUI dan Notebook | 
| 18223130 | Implementasi osmolaritas dan visualisasi | 
