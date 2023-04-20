---
  sidebar_position: 1
---

# Apa itu Clustering??

  Berbeda dengan klasifikasi, **Clustering** merupakan tugas **Data Mining** yang mengelompokan bukan berdasarkan variabel target layaknya seperti klasifikasi. **Clustering** mengelompokan data berdasarkan kemiripan satu sama lain. Menurut (Larose & Larose, 2014) **Clustering** adalah suatu teknik yang membagi data menjadi beberapa partisi (kelompok), sehingga objek dalam satu kelompok memiliki kemiripan satu sama lain namun berbeda dengan objek pada kelompok lainnya.

## Definisi

**Clustering** didefinisikan sebagai sebuah pemetaan dari suatu data ke dalam himpunan kelompok sedemikian sehingga setiap objek pada data memiliki tepat satu kelompok.
Secara matematis dapat dituliskan sebagai berikut:

Diberikan $D={t_1,t_2,t_3,\ldots,t_n}$ dan $K={K_1,K_2,K_3,\ldots,K_k}$.
Masalah clustering didefinisikan sebuah pemetaan $f:D\rightarrow K$ di mana, setiap $t_i$ dikelompokan ke dalam salah satu cluster $K_j$, 
sehingga $K_j=\{t_i \ |f(t_i)=K_j, 1 \leq i \leq n\ and \ t_i\in D \}$

Hasil masing-masing partisi dari proses **Clustering** memiliki objek-objek yang mirip satu sama lain. Mirip dalam hal ini adalah berdasarkan jarak, semakin dekat jarak dua objek maka kedua objek tersebut semakin memiliki tingkat kemirapan yang tinggi pula. Metode yang digunakan untuk mengukur jarak ada tiga yaitu *Euclidean distance*, *City-block distance*, dan *Minkowski distance*.

## Metode Perhitungan Jarak

Seperti yang sudah disebutkan dalam definisi diatas bahwa dasar pengelompokan *Clustering* adalah jarak. Semakin dekat jarak kedua objek maka semakin tinggi kemiripan kedua objek tersebut pula. Berikut metode perhitungan jarak seperti yang disebutkan pada definisi diatas.
1. *Euclidean distance*

  Metode perhitungan jarak ini, memiliki prinsip menjumlahkan setiap nilai yang diperoleh dari kuadrat pengurangan nilai yang bersesuaian. kemudian mengakarkan hasil tersebut. Secara matematis dituliskan sebagai berikut

  $$
  \begin{aligned}
    d_{Euclidean}\left(x,y\right)=\sqrt{\sum_{i}\left(x_i-y_i\right)^2}
  \end{aligned} 
  $$

2. *City-block distance*

  Hasil perhitungan jarak dengan metode ini diperoleh dari penjumlahan setiap mutlak pengurangan nilai yang bersesuaian. Secara matematis dituliskan sebagai berikut

  $$
  \begin{aligned}
    d_{cityblock}\left(x,y\right)=\sum_{i}\left|x_i-y_i\right|
  \end{aligned}
  $$

3. *Minkowski distance*

  Hasil perhitungan menggunakan metode ini adalah menjumlahkan pengurangan nilai yang bersesuaian yang telah dipangkatkan dengan suatu nilai $q$. Secara matematis dituliskan sebagai berikut

  $$
  \begin{aligned}
    d_{Minowski}\left(x,y\right)=\sum_{i}\left|x_i-y_i\right|^q
  \end{aligned}
  $$

### Contoh Perhitungan Jarak

Misalkan ada dua objek berdimensi sama dengan $4$ yaitu $x=2,5,6,4$ dan $y=10,3,11,15$ dengan menggunakan masing-masing metode diatas diperoleh hasil sebagai berikut
1. *Euclidean distance*

  $$
    \begin{align*}
      \phantom{{}={}}d_{Euclidean}\left(x,y\right)&=\sqrt{(2-10)^2+(5-3)^2+(6-11)^2+(4-15)^2}\\
      &=\sqrt{64+4+25+121}\\
      &=\sqrt{214}=14.63
    \end{align*}
  $$

2. *City-block distance*

  $$
    \begin{align*}
      \phantom{{}={}}d_{cityblock}\left(x,y\right)&={|2-10|+|5-3|+|6-11|+|4-15|}\\
      &={8+2+5+11}\\
      &={21}
    \end{align*}
  $$

3. *Minkowski distance*

  $$
    \begin{align*}
      \phantom{{}={}}d_{minkowski}\left(x,y\right)&={(2-10)^q+(5-3)^q+(6-11)^q+(4-15)^q}\\
      &={8^q+4^q+5^q+11^q}\\
    \end{align*}
  $$
  Jika dipilih $q=2$ maka diperoleh
    $$
    \begin{align*}
      \phantom{{}={}}d_{minkowski}\left(x,y\right)&={(2-10)^2+(5-3)^2+(6-11)^2+(4-15)^2}\\
      &={8^2+4^2+5^2+11^2}\\
      &={214}
    \end{align*}
  $$