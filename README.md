# Multivariate Statistical Cookbook Using R

## Principal Component Analysis

In data analysis, PCA reduces the dimensions in a multivariate data set. It maximizes variance on uncorrelated variables, which are created at the time of data analysis (Jolliffe and Cadima, 2016). The first principal component extracts the maximum explained variance or inertia from the data table.The second component must be orthogonal to the first, and have the second largest variance. The rest of the components take on the next biggest level of variance until the final component retains the smallest level of variance. Factor scores are the new values corresponding to the observations and can be projected on to the principal components graphically.

![Alt text](PCA1.png?raw=true "Title")

## Correspondence Analysis

Correspondence Analysis is similar to PCA, but is meant for qualitative data. Factor scores are generated for rows and columns, and both sets of factor scores have the same variance. Thus, they can be plotted on the same map for the analysis. CA also has distributional equivalence. Thus, merging two rows with the same profile does not affect the output and the output would be identical. A profile is a relative proportion versus an absolute number as in PCA. While PCA minimizes the sum of square of distance, CA minimized the sum of squares of mass times distance squared or Inertia.
The data set contains 120 consumers who evaluated their emotions upon tasting 5 types of low income sausages. The objective was to then related these reported emotions to their sensory profiles. The participants were all female from either Mexico City or Monterrey.
The data table is a contingency table. Thus, variables are on the rows and columns while observations are the items of the table. Further, in a contingency table, the observations are independence from one other.
The research question of this section is: Do types of low-income sausages differ in the emotional responses people attribute to them?

![Alt text](CA1.png?raw=true "Title")

## Multiple Correspondence Analysis

MCA is an extension of PCA but analyzes categorical data instead. In some respects it is analogous to CA but uses binary data instead. MCA can also be adapted to quantitative data that is scored, for example, -5 to 5 and then binned to represent a pattern of 0 and 1 data entries.

![Alt text](MCA1.png?raw=true "Title")

## Barycentric Discriminant Analysis

BADA is a robust version of discriminant analysis, which groups observations into pre-defined groups such as COVID-19 positive or negative, employed or unemployed, or married, divorced, separated, or single. BADA can even be used when n << p. 

![Alt text](BADA1.png?raw=true "Title")

DiCA is an extension of Discriminant Analysis and Correspondence Analysis, with the caveat of containing nominal variables for the pre-defined groups. Traditionally, a comparison between a training data set and testing data set is done to evaluate the effectiveness of the classification ability of the analysis.

Using information from the same observations, PLSC finds the correlation of multivariate data in two data tables. The first step is to obtain latent variables from linear combination similar to PCA. Analogously, these latent variables maximize the covariance between the tables. Additionally, factor scores in PCA are akin to latent variables in PLSC while loadings in PCA are akin to saliences in PLSC. Bootstrap and permutation tests are added to the analysis when inferential PSLC is indicated.

This method combines Multi-Dimensional Scaling and STATIS. The STATIS step follows the MDS step and is an optimization step. Thus, optimum weights are added to the data table. Further, the sqaure of Eucledian distances are used to group variable for each matrix. DiSTATIS is specifically a I x I x K matrix where I are objects and K are people.


MFA is an extension of PCA with a multi-data table scenario. First, MFA does a PCA on each Table and normalizes each one. Second, the normalize tables are aggregated in a multi-dimensional table and another non-normalized PCA is run to generate factor scores and loadings. MFA specifically is a I by J by K matrix where I and J are objects and K are people.
