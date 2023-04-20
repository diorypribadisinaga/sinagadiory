---
sidebar_position: 3
---

# Algoritma ID3

ID3 merupakan salah satu algoritma yang digunakan untuk membangun pohon keputusan, algoritma ini pertama kali dikembangkan oleh J. Ross Quinlan pada tahun 1986. Algoritma ini melakukan proses rekursif dalam membangun pohon keputusan. Strategi dasar ID3 adalah memilih atribut dengan peroleh *Informatian Gain* tertinggi terlebih dahulu. Konsep yang digunakan untuk mengukur *Informatian Gain* adalah *Entropy*. *Entropy* digunakan untuk mengukur jumlah ketidakpastian atau keacakan dalam satu set data (Dunhan, 2003). Ketika semua data memiliki kelas yang sama, maka tidak adanya kepastian atau dalam hal *Entropy* sama dengan nol. Berikut langkah-langkah membangun pohon keputusan dengan algoritma ID3 (Han dkk., 2012) dengan $m$ menyatakan banyak kelas.

1. Menentukan nilai $Entropy$ dari $D$ seperti rumus dibawah ini 
 
   
   $$
   \begin{aligned}
      info\left(D\right)=-\sum_{i=1}^{m}p_i\log_2{p_i}\
   \end{aligned}
   $$

2. Menentukan nilai $Entropy$ setiap atribut 

  $$
  \begin{aligned}
      {info}_A\left(D\right)=\sum_{j=1}^{v}{\frac{\left|D_j\right|}{\left|D\right|}\times i n f o(D_j)}
  \end{aligned}
  $$

3. Perhitungan $info\left(D\right)$ dan ${info}_A\left(D\right)$ selanjutnya dihitung *Informatian Gain* setiap atribut dengan rumus: 

   $$
   \begin{aligned}
      Gain\left(A\right)=info\left(D\right)-{info}_A\left(D\right)
   \end{aligned}
   $$

Berdasarkan perhitungan $Gain(A)$ kemudian dipilih atribut yang memiliki *Informatian Gain* tertinggi, dan perhitungan ini berulang sampai semua data masuk ke dalam suatu kelas $(C_j\in C)$.


