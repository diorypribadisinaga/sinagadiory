---
sidebar_position: 2
---

# Decision Tree

Menurut (Singh, S. and Gupta, 2014) ***Decision Tree*** merupakan salah satu metode klasifikasi yang mudah dipahami tanpa mengetahui matematika secara mendalam. ***Decision Tree*** adalah struktur pohon seperti diagram alur, di mana setiap internal *node* (*node non leaf*) menunjukkan atribut, setiap cabang mewakili hasil dari uji, dan setiap *node* daun (*node leaf*) menunjukan label kelas (Han dkk., 2012). *Node* teratas pada struktur pohon keputusan disebut *root*. Berikut contoh struktur sederhana 

## Definisi

Secara umum pohon keputusan didefinisikan seperti di bawah
Definisi. Diberikan $D=\{t_1,t_2,t_3,\ldots,t_n\}$, atributes $A=\{A_1,A_2,A_3,\ldots,A_h\}$ dan himpunan kelas $C=\{C_1,C_2,C_3,\ldots,C_m\}$. Sebuah pohon disebut pohon keputusan jika memiliki properti berikut
* Terdiri dari satu *node* akar (*root*) yang diberi label dari salah satu atribut $A$.
*	Setiap *node* internal diberi label dengan atribut $A_i$.
*	Setiap *node* daun (*leaf*) diberi label kelas $C_j$.

Memecahkan masalah klasifikasi dengan Decision Tree dapat dilakukan dengan dua langkah berikut
1.	Bangun pohon keputusan dengan menggunakan data latih $D=\{t_1,t_2,t_3,\ldots,t_n\}$.
2.	Untuk setiap $t_i\in D$ tetapkan kelasnya berdasarkan himpunan kelas $C$.

## Algoritma ***Decision Tree***

Secara umum algoritma ***Decision Tree*** seperti dibawah ini

```
Algorithm: Generate_decision_tree. Generate a decision tree from the training tuples of data partition, D
Input : 
	Data partition, D, which is a set of training tuples and their associated class labels;
	attribute list, the set of candidate attributes;
	Attribute selection method, a procedure to determine the splitting criterion that “best” partitions the data tuples into individual classes. This criterion consists of a splitting attribute and, possibly, either a split-point or splitting subset.
Output : A decision tree.
Method : 
	1. create a node N;
	2. if tuples in D are all of the same class, C, then
	3. return N as a leaf node labeled with the class C;
	4. if attribute list is empty then
	5. return N as a leaf node labeled with the majority class in D; // majority voting
	6. apply Attribute_selection_method(D, attribute list) to find the “best” splitting criterion;
	7. label node N with splitting criterion;
	8. if splitting attribute is discrete-valued and multiway splits allowed then // not restricted to binary trees
	9. attribute list ← attribute list − splitting attribute; // remove splitting attribute
	10. for each outcome j of splitting criterion
// partition the tuples and grow subtrees for each partition
	11. let Dj be the set of data tuples in D satisfying outcome j; // a partition
	12. if Dj is empty then
	13. attach a leaf labeled with the majority class in D to node N;
	14. else attach the node returned by Generate_decision_tree(Dj , attribute list) to node N;
endfor
	 15. Return N

```

Berdasarkan algoritma diatas, yang menjadi pembeda untuk setiap algoritma pada ***Decision Tree*** adalah *Attribute_selection_method*, dimana algoritma ID3 menggunakan *Information Gain*, CART menggunakan *Gini Index* sedangkan algoritma C4.5 menggunakan *Gain Ratio*. Ketiga algoritma tersebut akan dijelaskan Subbab selanjutnya.
