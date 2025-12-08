# Ketimpangan-Pendidikan-Indonesia_Kelompok-24
Projek akhir mata kuliah Data Wrangling oleh kelompok 24, dengan judul Analisis Ketimpangan Pendidikan Antar Provinsi di Indonesia dalam Upaya Mewujudkan Pemerataan Akses dan Kualitas Pendidikan

## Data Understanding
Dataset Dataset_sekolahSMA berisi beberapa variabel yang akan digunakan untuk analisis ketimpangan pendidikan tingkat SMA antar Provinsi di Indonesia pada tahun 2023.
Dataset ini diperoleh dari gabungan 5 dataset yang berasal dari Badan Pusat Statistik (BPS), Open Data Jabar, dan Portal Satu Data Indonesia. Adapun dataset final yang digunakan yaitu berisi 20 variabel dengan total 34 data (provinsi) sesuai dengan gambar dibawah ini:

<img width="564" height="472" alt="Screenshot 2025-12-08 233843" src="https://github.com/user-attachments/assets/f6a1a76c-b9c9-437c-a346-8d04f7eb7655" />

## Deskripsi Variabel
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
