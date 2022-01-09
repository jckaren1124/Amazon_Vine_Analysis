# Amazon_Vine_Analysis

### Challenge Deliverable 1
An Amazon Review dataset for groceries was selected and extracted as a DataFrame. Dataset file is listed below with the DataFrame. 

https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Grocery_v1_00.tsv.gz

![image](https://user-images.githubusercontent.com/89353378/148317467-24c4ce17-9adc-4142-be22-9d135ffee6b3.png)



Four separate DataFrames were extracted from this dataset.

![image](https://user-images.githubusercontent.com/89353378/148317667-92c14b7f-1563-4ef4-92f4-001b9d5cf74a.png)

![image](https://user-images.githubusercontent.com/89353378/148317753-a6d0f795-b9e4-462f-83bf-cf6a9225c492.png)

![image](https://user-images.githubusercontent.com/89353378/148317814-5f7a2963-219f-4f95-ae91-c35b0d9ddf8c.png)

![image](https://user-images.githubusercontent.com/89353378/148317863-36af4a3d-9042-445d-ac4c-7e978fbf1895.png)

All of these four DataFrames were loaded in separate pgAdmin tables.

customers_table

![postgres customers_table](https://user-images.githubusercontent.com/89353378/148318035-5a8126bb-5871-4eed-94b4-7665a5dbc444.PNG)

products_table

![postgres products_table](https://user-images.githubusercontent.com/89353378/148318016-9db94584-d12f-4eb1-8887-128d8805c93d.PNG)

review_id_table

![postgres review_id_table](https://user-images.githubusercontent.com/89353378/148317998-28fa49ba-f401-4b63-a636-9af697e89492.PNG)

vine_table

![postgres vine_table](https://user-images.githubusercontent.com/89353378/148317976-d7224620-6222-482f-89da-7895fd2d4a2e.PNG)


### Challenge Deliverable 2

A vine table DataFrame was extracted from the grocery reviews list using pySpark and Google Colab.

![image](https://user-images.githubusercontent.com/89353378/148668598-3d234ed0-8307-4914-a2b6-a54591628bb8.png)


In order to choose reviews that have a higher likelihood of being the most helpful, this DataFrame was filtered to show total votes of 20 or more.

![image](https://user-images.githubusercontent.com/89353378/148668635-772d08cb-94b5-4df5-8e29-f45817704fdb.png)


This DataFrame was further reduced to show reviews where the percentage of helpful votes are greater than or equal to 50%.

![image](https://user-images.githubusercontent.com/89353378/148668761-aa5cad10-a9ac-43ec-b0a0-a98674bc8e85.png)


A new DataFrame was created that lists reviews written as part of the Vine program (paid).

![image](https://user-images.githubusercontent.com/89353378/148668826-80ad269a-3ec2-4a43-955d-ed1434a293a4.png)


Another DataFrame lists reviews that are not part of the Vine program (unpaid).

![image](https://user-images.githubusercontent.com/89353378/148668866-2160bf71-6642-4b55-b0c2-82e9e234a344.png)


Calculations were then made to determine the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for the two types of review (paid vs unpaid).

![image](https://user-images.githubusercontent.com/89353378/148669094-06704fed-d3ed-4d89-a0e9-7b8d97f6f422.png)  ![image](https://user-images.githubusercontent.com/89353378/148669143-163eb663-e392-46b2-9c3c-ed4838e3ec9b.png)

![image](https://user-images.githubusercontent.com/89353378/148669052-63e07205-130a-4283-896c-5bf5680eebfb.png)
  ![image](https://user-images.githubusercontent.com/89353378/148669167-4fc98c95-f5e5-45ca-bf36-e04aa6add3e0.png)

![image](https://user-images.githubusercontent.com/89353378/148668931-eeacfdab-a6e1-405b-a3a5-7e7f5ae96154.png)
  ![image](https://user-images.githubusercontent.com/89353378/148668939-cba10c1b-5fd8-4f12-82b7-c37997db15a7.png)


### Challenge Deliverable 3

**Overview of the analysis**

The purpose of this analysis is to determine whether product reviews from paid Amazon Vine members generate more favorable reviews and higher star ratings compared to nonpaid product reviews.  This comparison can show whether Amazon reviews are biased towards companies who pay Amazon for product reviews.
  
**Results**

The results indicate that 99.87% of 5-star rating reviews are from unpaid sources while 0.13% of the total 5-star rating reviews are from subscribers in the paid Vine program. Also, there are a total of 28,235 reviews with 15,692 of these reviews rated as 5-star ratings.  With such a high number of reviews, it's more likely that the results are valid.

**Summary**

The above results seem to indicate that Amazon ratings are valid, and that it may seem worthwhile to spend money in this Vine review program in exchange for honest feedback of company products.


