# Building recommendation system using Amazon Electronics Review dataset 


<br><br>

 ![image](https://user-images.githubusercontent.com/12857624/125155009-e9509c80-e111-11eb-8374-9b52d6da7cda.png)

<br><br>
### A good recommendation system boosts online sales revenue and many customers are dependant on onlilne market place's recommended product before making the final purchase.
<br>
Here, I will go over recommendation system building process using Amazon's Electronics review data. 


### 1. Data Review and Prep
a) The data is retrieved from Kaggle dataset : https://www.kaggle.com/prokaggler/amazon-electronic-product-recommendation. 
Originally the dataset has 78 million record. To reduce dataset volume, I used the sampling method first. It gave nice balance of 1-5 rating distribution.
<br>
[original dataset]
![image](https://user-images.githubusercontent.com/12857624/125157021-6c2b2480-e11d-11eb-9ce3-45b29f3cf294.png)


[sampled dataset]
![image](https://user-images.githubusercontent.com/12857624/125157048-8533d580-e11d-11eb-99dc-519a26363b23.png)


But when it comes to product : rating volume ratio, the sampling resulted in data sparsity that product : rating ratio was only 1:3 while the original set has 1:9 ratio. 
![image](https://user-images.githubusercontent.com/12857624/125157115-d8a62380-e11d-11eb-9a1e-ab8dc1f5ecae.png)

b) Upon examining number of users (x-axis) and number of ratings (y-axis), 90% of users in sample dataset has given only 1 review, which can be problematic since it results data sparsity.

![image](https://user-images.githubusercontent.com/12857624/125155197-10f43480-e113-11eb-8982-257a3d79f749.png)


### 2. Model Building 
<br>
For the model building I used surprise package (https://surprise.readthedocs.io/en/stable/index.html) which is an easy-to-use Python scikit for recommender systems.
With surprise 1) k-NN Based Algorithm 2)Matrix Factorization Based Algorithms 3)Other Collaborative Filtering Algorithms were evaluated.


Here, 11 models were compared like below and for this selected Amazon eletronics dataset with 100 review users, the BaselineOnly algorithm gave us the best rmse.


![image](https://user-images.githubusercontent.com/12857624/126117849-052091c8-8b22-4e66-8b8a-8db822b8f6a4.png)

SVDpp performs best 


### 3. Model Tuning 

To find the best k for SVDpp, below plot was drawn. Usibg GridsearchCV, optimal k=6 was found. 

![image](https://user-images.githubusercontent.com/12857624/126118269-3322d630-14db-448a-8bdf-5f9b80751503.png)



 

