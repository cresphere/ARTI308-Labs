# Lab 4: Data Quality Assessment & Preprocessing
## Tasks

- **Task 1**
Identify data quality issues in the dataset.

- **Task 2**
Apply one missing value strategy and explain why.

- **Task 3**
Detect and handle outliers using IQR.

- **Task 4**
Normalize numerical features using both Min-Max and Z-score.

- **Task 5**
Apply PCA and interpret explained variance.

## Answers

#### Task 1
Some mappings were needed to correct data types. Otherwise no quality issues were found.

#### Task 2
The missing value strategy applied is removing the records which contain missing values, since the number of records with missing values introduced are small.

#### Task 5
Explained Variance Ratio: [0.7902221 0.2097779]

This variance ratio suggests that PC1 explains ~80% of the variance held by Previous qualification (grade) and Admission Grade can be summarized into a single dimension (they are highly correlated)

PC2 contains the rest of the variance which PC1 could not contain (the other ~20%)

Keeping only PC1 and dropping PC2 would cause a ~20% loss of information

<img width="536" height="396" alt="image" src="https://github.com/user-attachments/assets/e76d2eb3-d638-43ef-8bfd-b2aa987edcb5" />

Every point in the plot represents a student. And the axes of this figure do not represent original features (those being Previous qualification (grade) and Admission Grade) and rather the horizontal axis represents PC1 while the vertical axis represents PC2.

PC1 contains the direction of the max variance in the data (being ~80%) and it represents a unified academic score (since previous and admission grade were combined) while PC2 contains the difference between the two features, it represents information which was not included in PC1 (such as when theres a big difference between the admission grade and the grade of the previous qualification)

Since most of the spread is horizontal, PC1 has captured most of the information in the two features.

***

More details for this lab are included and explained in the Jupyter notebook, as well as answers for the rest of the tasks.
