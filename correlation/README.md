# Correlation

Correlation is a technique used to determine how changes occur between two paired variables, providing insight into whether a statistical relationship exists between them. This technique indicates whether two variables tend to move together and, if so, in what direction. There are two possibilities:

1. If the correlation value is positive, then one variable will cause its paired variable to increase.
2. Jika bernilai negatif, maka variabel satu akan menurunkan variabel pasangannya.

## Pearson 

The Pearson correlation measures the strength and direction of the relationship between two variables. The coefficient value ranges from -1 to 1; the highest values ​​indicate similarity, a value of 0 signifies the absence of a relationship, and negative values ​​indicate a negative association. There are several prerequisites for using the Pearson correlation

1. The variable is continuous.

2. The relationship between the variables is approximately linear.

3. Does not have extreme outlier values

The formula used to calculate the Pearson correlation is

$$r = \frac{\sum (x_i - \bar{x}) (y_i - \bar{y})}{\sqrt{\sum (x_i - \bar{x})^2 (y_i - \bar{y})^2}}$$

![Pearson Correlation](https://github.com/FikriAbdillah01/statistics/blob/ff57baabaa0fd644ac4a2cfc5d2539b8d72a5cca/correlation/correlation_plots.png)

## Spearman 

The Spearman correlation coefficient is a non-parametric statistical method used to measure the strength and direction of the relationship between two variables based on their data ranks. Unlike the Pearson correlation, which relies on the linearity of two normally distributed numerical variables, Spearman assesses how well the relationship can be described using a monotonic function.

A monotonic relationship means that as the value of one variable increases, the value of the other variable tends to consistently increase or decrease, even though the pattern does not form a perfectly straight line. Spearman correlation can be used with either continuous or ordinal data or small sample sizes, and it is relatively robust to outliers. The mathematical formula for calculating this correlation is

$$\rho = 1 - \frac{6\sum d^2_i}{n(n^2-1)}$$

![spearman correlation](https://github.com/FikriAbdillah01/statistics/blob/693ba6d8c6e5a3aa199336fef061577dbb18e97a/correlation/spearman_corr.png)

## Kendall Tau 

Kendall's Tau ($\tau$) is a non-parametric measure used to determine the relationship between two ordinal variables. These variables consist of categorical data where the categories have a meaningful ranking—such as customer satisfaction ratings for a company's goods or services. The $\tau$ equation is

$$\tau = \frac{C - D}{C + D}$$

where $C$ represents concordant pairs and $D$ represents discordant pairs. Before using the formula, we must understand the meaning of concordant and discordant pairs:

- Concodant (C): The data pair $(X_i, Y_i)$ and $(X_j, Y_j)$ are called concordant if their rank is the same. That is, if $X_i > X_j$ then $Y_i > Y_j$, and vice versa.

- Discordant (D): A pair of data points is called discordant if their rankings are opposite. This means that if $X_i < X_j$, then $Y_i > Y_j$, or vice versa.

There are three versions of the Kendall's tau ($\tau$) formula: $\tau_a$, $\tau_b$, and $\tau_c$..

**Kendall's tau $\tau_a$** is used when all ranks are unique (there are no identical values ​​or ties), and its mathematical formulation is

$$\tau_a = \frac{C-D}{\frac{1}{2}n(n-1)}$$

where $n$ is the number of samples and $\frac{1}{2}n(n-1)$ is the total number of possible pairwise combinations of the $n$ objects.

**Kendall's tau $\tau_b$** is used when there are tied values ​​in variable X or Y. The formula for $\tau_a$ is modified to

$$\tau_b = \frac{C - D}{\sqrt{(N_0 - N_1)(N_0 - N_2)}}$$

$$N_0 = \frac{1}{2} n(n-1)$$
$$N_1 = \sum_i \frac{1}{2}t_i(t_i -1)$$
$$N_2 = \sum_j \frac{1}{2}u_j(u_j -1)$$

where $N_1$ represents the tie correction for variable X, with $t_i$ being the number of ties in the $i$-th group of ties in X, while $N_2$ is used for the tie correction for variable Y, with $u_j$ being the number of ties in the $j$-th group of ties in Y.

**Kendall's tau $\tau_c$** is specifically designed to measure the relationship between two ordinal variables presented in a rectangular contingency table (where the table dimensions—rows $\times$ columns—are asymmetrical, i.e., $\text{rows} \neq \text{columns}$). The formula is

$$\tau_c = \frac{2m (C - D)}{n^2 (m-1)}$$

where $n$ is the total sample size (total frequency in the table) and $m = \min(r, c)$ is the minimum value between the number of rows ($r$) and the number of columns ($c$).
