---
sidebar_position: 1
---

# Definisi Klasifikasi
Klasifikasi merupakan salah satu tugas dari ***Data Mining*** yang digunakan untuk mengelompokan data ke dalam kelas yang sudah ditentukan. Klasifikasi berguna untuk memetakan data ke dalam kelas yang sudah ditentukan sebelumnya. Klasifikasi merupakan metode yang membutuhkan data training berlabel untuk menghasilkan sebuah aturan yang mengklasifikasikan data uji ke dalam kelompok atau kelas yang telah ditentukan (Dunhan, 2003). Contoh aplikasi klasifikasi adalah pengenalan gambar dan pola, medis diagnosis, persetujuan pinjaman, mendeteksi kesalahan dalam aplikasi industri, dan mengklasifikasikan keuangan tren pasar. Estimasi dan prediksi dapat dilihat sebagai jenis klasifikasi. Permasalahan yang berkaitan dengan klasifikasi dapat dinyatakan seperti yang ditunjuk dalam definisi berikut

**Definisi**. Diberikan $D=\{t_1,t_2,t_3,\ldots,t_n\}$ merupakan data training dan himpunan kelas
$C=\{C_1,C_2,C_3,\ldots,C_n\}$. Masalah klasifikasi didefinisikan sebagai sebuah pemetaan dari $D$ ke $C$ atau ditulis sebagai $f:D\rightarrow C$ di mana, setiap $t_i$ dikelompokan ke dalam salah satu kelas, sehingga $C=\{C_j=f(t_i) \ |\ t_i\in D, C_j\in C\}$.

Dari definisi diatas untuk setiap $t_i$ akan memiliki kelas tepat satu pada himpunan $C$. Dapat ditulis sebagai $\forall t_i \in \mathbb{D}, \exist C_j$ sedemikian sehingga $f(t_i)=C_j$.