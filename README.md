# Credit_Risk_Analysis
## Overview of the analysis
Analysis to assessing credit risk. Good loans exceed dangerous loans by a wide margin, creating unbalanced groups in the data set.
As a result, a number of methodologies have been tested and utilized to determine how accurate their predictions are likely to be. 
## Results
As the objective of this research is to accurately identify fraudulent applications, even when there is a chance of false positives, the sign to watch is high sensitivity scores for high risk applications.

The balanced accuracy score will be displayed in the first image for the following lists, and a report with precision and recall scores will be displayed in the second image. 

- Naive Random Oversampling

  ![Screenshot 2023-01-04 at 12 50 02](https://user-images.githubusercontent.com/112133209/210649781-99cef3eb-d3eb-49f7-b8ef-44c781d71b7f.png)
  
  ![Screenshot 2023-01-04 at 12 50 18](https://user-images.githubusercontent.com/112133209/210649845-d6af5848-9f9d-4d5a-994a-182ed03dde00.png)
  What we can see is balanced score is neither high or low risk at 0.641. While the sensitivity to high risk dataset is at 0.70 and low risk is at 0.58

- SMOTE Oversampling

  ![Screenshot 2023-01-04 at 12 51 02](https://user-images.githubusercontent.com/112133209/210650541-2b26d368-92e7-4251-a641-99cef12c80f7.png)
  
  ![Screenshot 2023-01-04 at 12 51 15](https://user-images.githubusercontent.com/112133209/210650596-0cdbf7e8-0128-47f0-aa54-09ae1250271f.png)
  In SMOTE oversampling its 0.662 while the high risk is at 0.63 and the low risk is 0.69

- ClusterCentroids Undersampling

  ![Screenshot 2023-01-04 at 12 51 48](https://user-images.githubusercontent.com/112133209/210650669-4b754cf7-8eb3-4107-92eb-22404061b221.png)
  
  ![Screenshot 2023-01-04 at 12 52 10](https://user-images.githubusercontent.com/112133209/210650698-f095349c-a53b-4801-920d-32c4934e786c.png)
  ClusterCentroids have 0.544 reading with high risk at 0.69 and low risk at 0.40

- Combination Sampling

  ![Screenshot 2023-01-04 at 13 03 27](https://user-images.githubusercontent.com/112133209/210650747-f64ee635-4ca8-4546-9f4e-e91d6b3cf122.png)

  ![Screenshot 2023-01-04 at 13 03 39](https://user-images.githubusercontent.com/112133209/210650798-829b71fe-26b0-4e17-80b3-3944e7fce6c6.png)
  Combination have 0.641 whiel the high risk is at 0.70 while the low risk is at 0.58. Avg 0.58
  
- RandomForest Ensemble

  ![Screenshot 2023-01-04 at 14 14 28](https://user-images.githubusercontent.com/112133209/210660436-5e7e675d-8eec-4526-b945-fa9374ebe8d5.png)
  
  ![Screenshot 2023-01-04 at 14 14 40](https://user-images.githubusercontent.com/112133209/210660464-22d98b56-dbcf-4c07-8f38-c36d324aa5dc.png)
  In RandomForest we see 0.788 risk. With high at 0.70 and low at 0.87. An avg at 0.87

- AdaBoost Ensemble 

  ![Screenshot 2023-01-04 at 14 12 51](https://user-images.githubusercontent.com/112133209/210660552-8f18284b-acd2-42c5-a0b6-429a739a73da.png)
  
  ![Screenshot 2023-01-04 at 14 13 07](https://user-images.githubusercontent.com/112133209/210660588-e1c1c287-932d-4575-9454-8256c93c413f.png)
  Adaboost not sure if its balanced accuracy should be this high at 0.93. With high at being 0.92 and low at 0.94. Avgeraging at 0.94
  
## Summary

With all the methods being tested for this datasets. We can see that the SMOTE Oversampling has the lowest avg accuracy score. The highest accuracy score is RandomForest Ensemble at 0.788 and Adaboost Ensemble at 0.93. Therefore the SMOTE oversampling is the best method to caculate the lowest number of high risk application.

Issue or an error faced in the calcualtion: The AdaBoost ensemble for balanced accuracy not sure if 0.931 is suppose to be that high or not. If that is the accurate reading then the dataset of risk seems very high. 
