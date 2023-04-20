---
sidebar_position: 4
---

# Algoritma C4.5

Algoritma C4.5 merupakan algoritma perbaikan ID3 di mana kekurangan dari ID3 seperti tidak dapat menangani variabel kontinu, dan tidak tahan terhadap *missing value* dalam membangun pohon keputusan. Algoritma C4.5 menggunakan nilai *Gain Ratio* untuk memilih atribut, kemudian proses berulang sampai semua data masuk ke dalam suatu kelas  $(C_j\in C)$. Langkah membangun pohon keputusan dengan algoritma C4.5 hampir sama dengan algoritma ID3 hanya saja dilanjutkan dengan menghitung nilai *Gain Ratio*. Berikut langkah-langkah membangun pohon keputusan dengan algoritma C4.5 (Han dkk., 2012)

1. Menghitung nilai $Gain\left(A\right)$ yang diperoleh pada algoritma [ID3](/articles/klasifikasi/algoritma_id3).

2. Algoritma C4.5 tidak menggunakan $Gain\left(A\right)$ sebagai dasar pemilihan atribut saat membangun keputusan tetapi menggunakan $Gain Ratio$

   $$
   \begin{aligned}
      GainRatio\left(A\right)=\frac{Gain\left(A\right)}{SplitInfo(A)}
   \end{aligned}  
   $$

   Di mana,  

   $$
   \begin{aligned}
      SplitInfo\left(A\right)=-\sum_{j=1}^{v}{\frac{\left|D_j\right|}{\left|D\right|}\times\log_2{\left(\frac{\left|D_j\right|}{\left|D\right|}\right)}}
   \end{aligned}  
   $$

Berdasarkan $Gain Ratio$ yang diperoleh kemudian memilih yang paling tinggi untuk dijadikan sebagai atribut terbaik.