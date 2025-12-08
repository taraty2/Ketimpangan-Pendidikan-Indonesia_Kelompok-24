# Ketimpangan-Pendidikan-Indonesia_Kelompok-24
Projek akhir mata kuliah Data Wrangling oleh kelompok 24, dengan judul Analisis Ketimpangan Pendidikan Tingkat SMA Antarprovinsi di Indonesia Tahun 2023 

Pada repository ini akan berisi hasil proses pengolahan data pendidikan SMA per provinsi di Indonesia tahun 2023, dimana data diperoleh melalui proses pre-processing, penggabungan beberapa sumber hingga pembuatan variabel turunan. Sehingga akan terdapat dua dataset utama, yaitu:
1. Dataset_sekolahSMA 
2. indeks_pendidikan_2023 

## Deskripsi Dataset_sekolahSMA  
Dataset Dataset_sekolahSMA berisi beberapa variabel yang akan digunakan untuk analisis ketimpangan pendidikan tingkat SMA antar Provinsi di Indonesia pada tahun 2023.
Dataset ini diperoleh dari gabungan 5 dataset yang berasal dari Badan Pusat Statistik (BPS), Open Data Jabar, dan Portal Satu Data Indonesia. Adapun dataset final yang digunakan yaitu berisi 20 variabel dengan total 34 data (provinsi) sesuai dengan gambar dibawah ini:

<img width="564" height="472" alt="Screenshot 2025-12-08 233843" src="https://github.com/user-attachments/assets/f6a1a76c-b9c9-437c-a346-8d04f7eb7655" />

Berikut penjelasan mengenai variabel-variabel yang ada di dalam dataset:

| No | Variabel                           | Keterangan Lengkap                                                                                                                                                       | Tipe Data     |
| -- | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------- |
| 1  | **Provinsi**                       | Menyatakan lingkup provinsi yang ada di Indonesia                                                                                                                        | object (teks) |
| 2  | **jumlah sekolah SMA (negeri)**    | Menyatakan jumlah seluruh sekolah menengah atas (SMA) negeri yang ada di setiap provinsi                                                                                 | int64         |
| 3  | **jumlah guru SMA (negeri)**       | Menyatakan jumlah total guru SMA negeri di setiap provinsi                                                                                                               | int64         |
| 4  | **jumlah murid SMA (negeri)**      | Menyatakan jumlah total murid SMA negeri di setiap provinsi                                                                                                              | int64         |
| 5  | **internet negeri**                | Menyatakan persentase SMA negeri yang memiliki akses internet di setiap provinsi                                                                                         | float64       |
| 6  | **a negeri**                       | Menyatakan jumlah ruang kelas SMA negeri yang berada dalam kondisi baik (a)                                                                                              | int64         |
| 7  | **b negeri**                       | Menyatakan jumlah ruang kelas SMA negeri yang berada dalam kondisi rusak ringan (b)                                                                                      | int64         |
| 8  | **c negeri**                       | Menyatakan jumlah ruang kelas SMA negeri yang berada dalam kondisi rusak sedang (c)                                                                                      | int64         |
| 9  | **d negeri**                       | Menyatakan jumlah ruang kelas SMA negeri yang berada dalam kondisi rusak berat (d)                                                                                       | int64         |
| 10 | **jumlah sekolah SMA (swasta)**    | Menyatakan jumlah seluruh sekolah menengah atas (SMA) swasta yang ada di setiap provinsi                                                                                 | int64         |
| 11 | **jumlah guru SMA (swasta)**       | Menyatakan jumlah total guru pada SMA swasta di tiap provinsi                                                                                                            | int64         |
| 12 | **jumlah murid SMA (swasta)**      | Menyatakan jumlah total murid pada SMA swasta di tiap provinsi                                                                                                           | int64         |
| 13 | **internet swasta**                | Menyatakan persentase sekolah SMA swasta yang memiliki akses internet di tiap provinsi                                                                                   | float64       |
| 14 | **a swasta**                       | Menyatakan jumlah ruang kelas SMA swasta dalam kondisi baik (a)                                                                                                          | int64         |
| 15 | **b swasta**                       | Menyatakan jumlah ruang kelas SMA swasta dalam kondisi rusak ringan (b)                                                                                                  | int64         |
| 16 | **c swasta**                       | Menyatakan jumlah ruang kelas SMA swasta dalam kondisi rusak sedang (c)                                                                                                  | int64         |
| 17 | **d swasta**                       | Menyatakan jumlah ruang kelas SMA swasta dalam kondisi rusak berat (d)                                                                                                   | int64         |
| 18 | **rata_rata_lama_sekolah**         | Menyatakan rata-rata lama pendidikan yang ditempuh penduduk (dalam tahun) di tiap provinsi                                                                               | float64       |
| 19 | **angka melek aksara 15–59 tahun** | Menyatakan persentase penduduk usia 15–59 tahun yang dapat membaca dan menulis pada tiap provinsi                                                                        | float64       |
| 20 | **total_ruang_kelas**              | Menyatakan jumlah total ruang kelas SMA tiap provinsi dengan menjumlahkan seluruh kondisi ruang kelas: baik (a), rusak ringan (b), rusak sedang (c), dan rusak berat (d) | int64         |

## Deskripsi indeks_pendidikan_2023
Dataset indeks_pendidikan_2023 berisi nilai indeks pendidikan untuk setiap provinsi di Indonesia pada tahun 2023. Dataset ini disusun dari hasil pengolahan Dataset_sekolahSMA dan digunakan untuk menggambarkan tingkat pemerataan pendidikan SMA/K antarprovinsi.

<img width="433" height="117" alt="Screenshot 2025-12-09 000836" src="https://github.com/user-attachments/assets/b928ac6b-d15d-4181-bd38-d16d88b7e75f" />

Berikut penjelasan mengenai variabel yang ada di dalam dataset ini:

| No | Variabel | Keterangan Lengkap | Tipe Data |
|----|----------|---------------------|-----------|
| 1 | Provinsi | Menyatakan lingkup provinsi yang ada di Indonesia. Berfungsi sebagai identitas provinsi agar setiap baris data bisa dikaitkan dengan provinsi tertentu, memungkinkan perbandingan dan analisis antar-provinsi. | object |
| 2 | Indeks_Pendidikan | Menyatakan nilai yang menggambarkan kondisi pendidikan di suatu provinsi berdasarkan beberapa indikator, seperti jumlah sekolah sma (negeri+swasta), persentase_sekolah_negeri, persentase_sekolah_swasta, jumlah guru sma (negeri+swasta), Rasio_Guru_Murid_SMA_Negeri_inv, Rasio_Guru_Murid_SMA_Swasta_inv, Persentase Internet Total, a total, rata_rata_lama_sekolah, angka melek aksara 15-59 tahun, Rasio_Murid_Sekolah_SMA_Total_inv. Nilai dari indikator yang digunakan sudah dilakukan normalisasi sehingga berada pada rentang 0–1, di mana angka yang lebih tinggi menunjukkan kondisi pendidikan yang lebih merata. | float64 |

