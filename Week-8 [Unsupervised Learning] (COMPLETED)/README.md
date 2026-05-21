# WEEK-8 Unsupervised Learning
Dataset yang digunakan:
- `berat_tinggi.csv`

<br>

# WEEK-8 [UNSUPERVISED LEARNING]

Di dalam Week-8 ini kami ditugaskan untuk mengerjakan tugas Unsupervised Learning yang dimana sekarang ini kami berfokus kepada pengaplikasian  **K-Means Clustering** unsupervised learning dengan 2 metode yaitu (Metode Elbow dan Metode Score-Plot). <br>

<br>

Berikut dibawah ini adalah salah satu screenshot hasil pengerjaan assignment saya. `berat_tinggi.csv`
![GambarHasil](Pictures/Assignment.png) 

# ASSIGNMENT-6 Wine Quality Dataset

Setelah melakukan practice harian, adapula assignment 6 yang diberikan yang dimana disini kami melakukan hal yang sama yaitu menggunakan Unsupervised Learning seperti pada practice harian yang dilakukan namun menggunakan dataset yang berbeda yaitu `WineQT.csv` dan berikut dibawah ini adaalah hasil ringkas pengerjaan saya.

![GambarHasil](Pictures/WineQTArm.png) 
Di atas adalah hasil Elbow Projection yang saya dapatkan dari dataset WineQT yang dimana disini saya memilih titik elbow ketiga `n_clusters=3` sebagai titik `kmeans` saya.

![GambarHasil](Pictures/WineQTScatter1.png) 
![GambarHasil](Pictures/WineQTScatter2.png)
Kedua gambar diatas adalah hasil perbandingan Anotator yang saya dapatkan dan dapat dilihat lebih jelas juga pada bagian hasil distribusi dibawah ini:

### Hasil Distribusi 
Distribusi cluster (Elbow): <br>
cluster_elbow <br>
1    720 <br>
2    390 <br>
0     33 <br>
Name: count, dtype: int64 <br>

Distribusi cluster (Via-Score): <br>
cluster_via <br>
1    720 <br>
2    390 <br>
0     33 <br>
Name: count, dtype: int64 <br>

Distribusi quality asli: <br>
quality <br>
3      6 <br>
4     33 <br>
5    483 <br>
6    462 <br>
7    143 <br>
8     16 <br>
Name: count, dtype: int64 <br>

## Conclusion Hasil
### Interpretasi Hasil Via-Score Method:

1. **Proses clustering berhasil** mengelompokkan data wine ke dalam cluster berdasarkan kemiripan karakteristik kimia (kadar alkohol, keasaman, sulfur, dll), bukan berdasarkan label quality secara langsung — sesuai dengan sifat unsupervised learning.

2. **Cluster 0** mengelompokkan wine dengan karakteristik kimia tertentu, misalnya kadar alkohol sedang dan total sulfur dioxide tinggi.

3. **Cluster 1** mengelompokkan wine dengan keasaman yang lebih tinggi (volatile acidity & fixed acidity lebih besar).

4. **Cluster 2** mengelompokkan wine dengan kadar alkohol lebih tinggi yang umumnya berkorelasi dengan kualitas yang lebih baik.

5. Meskipun label `quality` tidak digunakan saat training, terdapat keterkaitan antara hasil cluster dan distribusi quality — ini menunjukkan bahwa fitur kimia memiliki pola yang berkorelasi dengan kualitas wine secara alami.

### Directory
Untuk file pengerjaan Assignment-6 dapat dilihhat di dalam file: <br> `WineQuality_Aldon/Assignment_WineQuality_Aldon.ipynb`