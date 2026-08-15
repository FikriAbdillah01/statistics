# Correlation

Correlation is a technique used to determine how changes occur between two paired variables, providing insight into whether a statistical relationship exists between them. This technique indicates whether two variables tend to move together and, if so, in what direction. There are two possibilities:

1. If the correlation value is positive, then one variable will cause its paired variable to increase.
2. Jika bernilai negatif, maka variabel satu akan menurunkan variabel pasangannya.

## Pearson 

Pearson Correlation merupakan tolok ukur kekuatan dan arah hubungan antara dua variabel. Nilai koefisien ini berada di antara -1 dan 1 dengan nilai tertinggi menandakan adanya similaritas, sedangkan 0 mengartikan tidak adanya hubungan antara keduanya, dan nilai negatif menandakan keterikatan negatif. Ada beberapa syarat sebelum menggunakan Pearson Correlation

1. Variable bersifat kontinu

2. Hubungan antara variabel mendekati linear

3. Tidak memiliki nilai-nilai outlier yang ekstrim

Rumus yang digunakan untuk menghitung korelasi Pearson adalah

$$r = \frac{\sum (x_i - \bar{x}) (y_i - \bar{y})}{\sqrt{\sum (x_i - \bar{x})^2 (y_i - \bar{y})^2}}$$

![Pearson Correlation](https://github.com/FikriAbdillah01/statistics/blob/ff57baabaa0fd644ac4a2cfc5d2539b8d72a5cca/correlation/correlation_plots.png)

## Spearman 

Spearman correlation coefficient merupakan metode statistik non parametrik yang digunakan untuk mengukur kekuatan dan arah hubungan antara dua variabel berdasarkan peringkat datanya. Berbeda dengan Pearson yang menggunakan linearitas dari dua variabel yang ber numerik normal, Spearman menilai seberapa baik hubungan tersebut dapat digambarkan menggunakan fungsi monotonik.

Hubungan monotonik berarti ketika nilai satu variabel meningkat, nilai variabel lainnya cenderung ikut meningkat atau justru menurun secara konsisten, meskipun polanya tidak membentuk garis lurus sempurna. Spearman correlation can be used with either continuous or ordinal data, small sample of data, and it is relatively robust to outliers. Formulasi matematika untuk menghitung korelasi ini adalah

$$\rho = 1 - \frac{6\sum d^2_i}{n(n^2-1)}$$

![spearman correlation](https://github.com/FikriAbdillah01/statistics/blob/693ba6d8c6e5a3aa199336fef061577dbb18e97a/correlation/spearman_corr.png)

## Kendall Tau 

Kendall Tau $\tau$ merupakan tolok ukur nonparametrik yang bisa digunakan untuk mengetahui hubungan between two ordinal variables. Variabel tersebut mencakup data kateogis dimana kategori kategorinya memiliki peringkat bermakna, seperti rating pelanggan terhadap kepuasan suatu barang atau jasa dari perusahaan. Persamaan $\tau$ adalah

$$\tau = \frac{C - D}{C + D}$$

dengan $C$ mewakili pasangan konkordan (concordant pairs) dan $D$ adalah pasangan yang diskordan (discordant pairs). Sebelum menggunakan rumus, kita harus mengetahui maksud dari concordant and discordant pairs:

- Concodant (C): Pasangan data $(X_i, Y_i)$ dan $(X_j, Y_j)$ disebut concordant jika peringkatnya sama. Artinya, jika $X_i > X_j$ maka $Y_i > Y_j$, begitu juga sebaliknya.

- Discordant (D): Pasangan data disebut discordant jika peringkatnya berlawanan. Artinya, jika $X_i < X_j$ maka $Y_i > Y_j$ atau sebaliknya.

Ada 3 versi rumus Kendall's tau $\tau$, yaitu $\tau_a$, $\tau_b$, dan $\tau_c$.

**Kendall's tau $\tau_a$** digunakan jika semua peringkat unik (tidak ada nilai yang sama atau ties) dengan formulasi matematisnya adalah

$$\tau_a = \frac{C-D}{\frac{1}{2}n(n-1)}$$

dengan $n$ adalah jumlah sampel dan $\frac{1}{2}n(n-1)$ merupakan jumlah total kombinasi pasangan yang mungkin dari objek n.

**Kendall's tau $\tau_b$** digunakan jika terdapat nilai yang sama dalam variabel X atau Y. Rumus $\tau_a$ dimodifikasi menjadi

$$\tau_b = \frac{C - D}{\sqrt{(N_0 - N_1)(N_0 - N_2)}}$$

$$N_0 = \frac{1}{2} n(n-1)$$
$$N_1 = \sum_i \frac{1}{2}t_i(t_i -1)$$
$$N_2 = \sum_j \frac{1}{2}u_j(u_j -1)$$

dengan $N_1$ merupakan koreksi nilai kembar pada variabel X dengan $t_i$ adalah banyaknya nilai kembar ke-$i$ pada X, sedangkan $N_2$ digunakan untuk koreksi nilai kembar pada variabel Y dengan $u_j$ adalah banyaknya nilai kembar ke-$j$ pada Y.

**Kendall's tau $\tau_c$** dirancang khusus untuk mengukur hubungan antara dua variabel ordinal yang disajikan dalam bentuk tabel kontingensi persegi panjang (dimana tabel ukuran $row \space \times \space column$ tidak simetrik alias $row \neq column$). rumusnya adalah

$$\tau_c = \frac{2m (C - D)}{n^2 (m-1)}$$

dengan $n$ adalah total seluruh sampel (total frekuensi dalam tabel) dan $m = min(r,c)$ adalah nilai minimum antara jumlah baris ($r$) dan jumlah kolom ($c$).
