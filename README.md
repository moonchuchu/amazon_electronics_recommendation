# Building recommendation system using Amazon Electronics Review dataset 

 ![image](https://user-images.githubusercontent.com/12857624/125155009-e9509c80-e111-11eb-8374-9b52d6da7cda.png)

Good recommendation system boost online sales revenue and many customers are dependant on onlilne market place's recommended product before making the final purchase.
Here, I will go over recommendation system building process using Amazon's Electronics review data. 


1. Data 
The data is retrieved from Kaggle dataset : https://www.kaggle.com/prokaggler/amazon-electronic-product-recommendation. 
Originally the dataset has 78 million record. To reduce dataset volume, I used the sampling method first. It gave nice balance of 1-5 rating distribution but when it comes to product : rating volume ratio, the sampling resulted in data sparsity that product : rating ratio was only 1:3 while the original set has 1:9 ratio. 


![image](https://user-images.githubusercontent.com/12857624/125155197-10f43480-e113-11eb-8982-257a3d79f749.png)



2. 
