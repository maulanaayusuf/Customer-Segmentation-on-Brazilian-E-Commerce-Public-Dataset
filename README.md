
# Maulanaayusuf/ Customer-Segmentation-on-Brazilian-E-Commerce-Public-Dataset
RFM analysis using R Programming

# Summary
This dataset was generously provided by Olist, the largest department store in Brazilian marketplaces. This dataset total has 100k Rows and 54 Column.
RFM segmentation is one method for segmenting customers by measuring the level of recency, frequency and monetary

**The result of this project is** 

- Getting information about monthly GMV

- Gaining insight about potential sellers

- Customer segments.

- Category Product Recommendation


# Data Understanding
The dataset has information of 100k orders  (100k rows) from 2016 to 2018 made at multiple marketplaces in Brazil. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers. It also released a geolocation dataset that relates Brazilian zip codes to lat/lng coordinates (total has 54 column)

**But the column we are using this time is:**

Customer_unique_id    	     	: unique identifier of a customers

Order_item_id 		            : number of items purchased

Seller_id		  	              : seller unique identifier

Price			     	              : item price

Order_purchase_timestamp     	: Shows the purchase timestamp


# Exploratory Data Analysis

![image](https://user-images.githubusercontent.com/85357151/132887980-479b6380-4e1c-4c41-b582-b6f6067a0610.png)

- GMV value increased rapidly from 01-01-2017

- Had a peak in sales in November 2017, up about 54% from the previous month. which indicates that the strategy carried out in that month or the previous month has proven effective

**Gross Merchandise Value by Product Category**

![image](https://user-images.githubusercontent.com/85357151/132888237-a0159627-f70f-4d77-b07f-d094eb8a7386.png)
out of a total of 71 categories, these top 10 categories contribute about 63.37% GMV


**Seller Sales**

![image](https://user-images.githubusercontent.com/85357151/132888345-bf5d3825-7604-4885-820b-30d51637d44f.png)


20% of sellers earn 80% GMV, while the other 80% of sellers only earn 20% GMV

From of a total of 2990 sellers:

- 1-17 top sellers give about 20% of total GMV

- 1-73 top sellers give around 40% of total GMV

- 1-211 top sellers give about 60% of total GMV

- 1-531 top sellers give about 80% of total GMV


**Customers Orders**

![image](https://user-images.githubusercontent.com/85357151/132888797-afc30f5d-a298-4a40-a026-a2e31e11e1aa.png)

From our total 93664 customers:
 
79640 or 85% made 1x orders

10432 or 11% customers made 2x orders

1902 or 2% customers made 3x orders

- Our main problem this time is that 85% of our customers only make 1x purchases. It indicates that our returning customers or retention rate is very low


# Customer Segmentation with RFM Analysis

![image](https://user-images.githubusercontent.com/85357151/132889047-73766284-962d-4846-947e-d5b596fc5ece.png)

Recency (R) :  the number of days since a customer made the last purchase

Frequency (F) : how often customer bought the product in a given period.

Monetary (M) : is the total amount of money a customer spent in that given period. 



**Customer Segmentation with RFM Analysis**

- Assign a score criteria from 1 to 5 for each Recency, Frequency, and Monetary

- 5 is highest value and 1 is lowest value

- because the number of customers who make purchases more than 1x is only 15%, the F value is only 1 and 5


![image](https://user-images.githubusercontent.com/85357151/132889919-dbcfa7e5-701f-4a6d-9de2-a13808a98983.png)



# Customer Segmentation

![image](https://user-images.githubusercontent.com/85357151/132890196-711a6b4f-8e75-42cd-9197-25867ebecc2c.png)

- Potential customers have a very large number, meaning that many customers can still be maximized

- Loyal customers and  Best customers are very few in number

![image](https://user-images.githubusercontent.com/85357151/132890398-8996ae2a-99e7-4b84-a66f-eaca25ff7543.png)
![image](https://user-images.githubusercontent.com/85357151/132890405-406375ce-1195-4332-8c63-af363968bded.png)
![image](https://user-images.githubusercontent.com/85357151/132890413-b3d114fc-1fa4-47a8-a536-0d18a02f995d.png)


- potential customers have a fairly high median monetary value only from 1x purchase. So indeed, the potential customer segment can be maximized to become the best customer and loyal customer 

- lost customers have a fairly high median monetary, but they haven't made a purchase in a long time, so we need to send notifications and give promo so that they become active buyers again


# GMV Product By Segment Customers

**Potential Customers**
![image](https://user-images.githubusercontent.com/85357151/132890728-e543d41a-4ee3-479a-bf9d-61a1f85ca955.png)

**Almost Lost Customers**
![image](https://user-images.githubusercontent.com/85357151/132890793-acb107aa-c56f-4a90-8ed5-d6fef88ef24c.png)

**Best Customers**
![image](https://user-images.githubusercontent.com/85357151/132890824-eab0be5c-e558-46d5-a318-b93de80ea4c7.png)


- The best_customers segment has  top categories: bed_bath_table, housewares and furniture_decor which may be used as bundling packages to attract customers




**Lost Cheap Customers**
![image](https://user-images.githubusercontent.com/85357151/132890932-f3b7d02b-cfb7-46a3-962c-ab92be9aa2f1.png)

**New Customers**
![image](https://user-images.githubusercontent.com/85357151/132890963-e71d1237-0baf-4940-a9ad-90f76503b4ac.png)

- Although telephony category is a lot in lost cheap customers, it is also the best-selling category for new customers. This indicates that the telephone category is effective for bringing in new customers


**Lost Customers**
![image](https://user-images.githubusercontent.com/85357151/132891317-8e6e6e57-9426-4a6e-a172-1620c46b73a3.png)

**Loyal Customers**
![image](https://user-images.githubusercontent.com/85357151/132891355-63520bcd-3076-4c0f-9eaf-8b184933ad1d.png)


- Categories bed_bath_table, furniture_decor,  computer_accessories, and sport_leisure are best-seller categories in  lost customer segments, but also the best-seller for loyal customers. 
- This indicates that these categories have the potential to be used as promos for lost customers so that they become active customers again


# Recommendation

- Create a loyalty program/membership program which customers will get rewards for every transaction
- Send engaging emails to customers, especially to potential customers
- Send Notification to potential, almost lost, and lost customers
- To get new customers, we can provide discount promos for the telephony and health_beauty category
- Create bundling package: bed_bath_table, housewares_and furniture_decor 
- Give promos, especially to the top 10 product categories in potential customers
- Give rewards or make competition for sellers to increase their productivity


# Thank you





















