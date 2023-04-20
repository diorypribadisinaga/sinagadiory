---
sidebar_position: 3
---

# k-means Clustering

k-Means merupakan salah satu algoritma *Partitioning methods*, sehingga banyak *cluster* (k) ditentukan terlebih dahulu. Algoritma ***k-means*** menggunakan titik *centroid* yaitu rata-rata *cluster* sebagai dasar pengelompokan objek ke dalam *cluster*. Secara matematis algoritma ***k-means*** *Clustering* sebagai berikut:
Diberikan $x_1,x_2,x_3,\ldots,x_n$ dengan masing-masing $x_i$ memiliki d dimensi dan k banyak *cluster*

1. Inisialisasi: Pilih k objek secara acak sebagai *centroid*. Misalkan $c_1,c_2,\ldots,c_m$ sebagai masing-masing pusat *cluster* (*centroid*).
2. Setiap objek yang tersisa dikelompokan ke dalam *cluster* yang paling dekat berdasarkan *Euclidean distance*.
3. Perbarui masing-masing *centroid* *cluster*. Nilai *centroid* diperoleh dari rata-rata *cluster*. Lakukan langkah 2-3 sampai tidak ada perubahan pada *cluster*

Algoritma ***k-means*** dapat dituliskan dalam bentuk *pseudo-code* seperti dibawah ini
```code
Algorithm: k-means. The k-means algorithm for partitioning, where each cluster’s center is represented by the mean value of the objects in the cluster.
Input : 
	k: the number of clusters
	D: a data set containing n object
Output : A set of k clusters
Method :
(1)	arbitrarily choose k objects from D as the initial cluster centers;
(2)	repeat
(3)	(re)assign each object to the cluster to which the object is the most similar, based on the mean value of the objects in the cluster;
(4)	update the cluster means, that is, calculate the mean value of the objects for each cluster;
(5)	until no change;

```

Berdasarkan algoritma diatas ***k-means*** langkah pertama yang dilakukan adalah memilih $k$ objek sembarang sebagai inisialisasi *centroid* masing-masing *cluster*. Dalam pemilihan $k$ objek secara sembarang dapat menggunakan konsep [teknik sampling](/articles/teorisampling/intro.md) yang dijelaskan selanjutnya.