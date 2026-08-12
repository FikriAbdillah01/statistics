# Correlation

Correlation adalah teknik untuk mengetahui bagaimana perubahan antara dua variabel yang dipasangkan, menyediakan insight apakah ada hubungan diantara mereka berdua. Teknik ini menunjukkan apakah dua variabel memiliki kecenderungan untuk bergerak bersama, dan jika iya, maka kearah mana. Akan ada dua kemungkinan:

1. Jika nilai korelasi itu positif, maka variable satu akan menaikkan variabel pasangannya.
2. Jika bernilai negatif, maka variabel satu akan menurunkan variabel pasangannya.

## Pearson Correlation

Pearson Correlation merupakan tolok ukur kekuatan dan arah hubungan antara dua variabel. Nilai koefisien ini berada di antara -1 dan 1 dengan nilai tertinggi menandakan adanya similaritas, sedangkan 0 mengartikan tidak adanya hubungan antara keduanya, dan nilai negatif menandakan keterikatan negatif. Ada beberapa syarat sebelum menggunakan Pearson Correlation

1. Variable bersifat kontinu

2. Hubungan antara variabel mendekati linear

3. Tidak memiliki nilai-nilai outlier yang ekstrim

Rumus yang digunakan untuk menghitung korelasi Pearson adalah

$$r = \frac{\sum (x_i - \bar{x}) (y_i - \bar{y})}{\sqrt{\sum (x_i - \bar{x})^2 (y_i - \bar{y})^2}}$$

[Pearson Correlation](https://github.com/FikriAbdillah01/statistics/blob/ff57baabaa0fd644ac4a2cfc5d2539b8d72a5cca/correlation/correlation_plots.png)

## Spearman Correlation

Spearman correlation coefficient merupakan metode statistik non parametrik yang digunakan untuk mengukur kekuatan dan arah hubungan antara dua variabel berdasarkan peringkat datanya. Berbeda dengan Pearson yang menggunakan linearitas dari dua variabel yang ber numerik normal, Spearman menilai seberapa baik hubungan tersebut dapat digambarkan menggunakan fungsi monotonik.

Hubungan monotonik berarti ketika nilai satu variabel meningkat, nilai variabel lainnya cenderung ikut meningkat atau justru menurun secara konsisten, meskipun polanya tidak membentuk garis lurus sempurna. Spearman correlation can be used with either continuous or ordinal data, small sample of data, and it is relatively robust to outliers. Formulasi matematika untuk menghitung korelasi ini adalah

$$\rho = 1 - \frac{6\sum d^2_i}{n(n^2-1)}$$
