# TARGET-BRAZIL-SALES-ANALYSIS

## Introduction:
	Target is a globally renowned brand and a generalised merchandise retailer & headquartered in Minneapolis, Minnesota. It is the 7th largest retailer in U.S.

	This brand has a wide variety of food & general merchandise from clothing to household goods to electronics and toys.

	Target offers both online & in-store shopping.

	The particular business case focuses on the operations of Target in Brazil and provides insightful information about 1,00,000 orders placed between 2016 and 2018.

## Problem Statement:
Assuming you are a data analyst/ scientist at Target, you have been assigned the task of analyzing the given dataset to extract valuable insights and provide actionable recommendations.

# DATASET INFORMATION:
	The dataset has information about the order_status, price, payment and freight performance, customer location, product attributes and customer reviews.

	The data is available in 8 csv files:

1.	customers.csv
2.	sellers.csv
3.	order_items.csv
4.	geolocation.csv
5.	payments.csv
6.	reviews.csv
7.	orders.csv
8.	products.csv
 
## The column description for these CSV files is given below:

### The customers.csv contain following features:
	customer_id: Id of the consumer who made the purchase.

	customer_unique_id: Unique Id of the consumer.

	customer_zip_code_prefix: Zip Code of the location of the consumer.

	customer_city: Name of the City from where order is made.

	customer_state: State Code from where order is made (Ex- Sao paulo-SP).

### The sellers.csv contains following features:
	seller_id: Unique Id of the seller registered.

	seller_zip_code_prefix: Zip Code of the location of the seller.

	seller_city: Name of the City of the seller.

	seller_state: State Code (Ex- Sao paulo-SP).
 
### The order_items.csv contain following features:
	order_id: A unique id of order made by the consumers.

	order_item_id: A Unique id given to each item ordered in the order.

	product_id: A unique id given to each product available on the site.

	seller_id: Unique Id of the seller registered in Target.

	shipping_limit_date: The date before which shipping of the ordered product must be completed.

	price: Actual price of the products ordered.

	freight_value: Price rate at which a product is delivered from one point to another.

### The geolocations.csv contain following features:
	geolocation_zip_code_prefix: first 5 digits of zip code

	geolocation_lat: latitude

	geolocation_lng: longitude

	geolocation_city: city name

	geolocation_state: state
 
### The payments.csv contain following features:
	order_id: A unique id of order made by the consumers.

	payment_sequential: sequences of the payments made in case of EMI.

	payment_type: mode of payment used. (Ex-Credit Card).

	payment_installments: number of installments in case of EMI purchase.

	payment_value: Total amount paid for the purchase order.

### The orders.csv contain following features:
	order_id: A unique id of order made by the consumers.

	customer_id: Id of the consumer who made the purchase.

	order_status: status of the order made i.e., delivered, shipped etc.

	order_purchase_timestamp: Timestamp of the purchase.

	order_delivered_carrier_date: delivery date at which carrier made the delivery.

	order_delivered_customer_date: date at which customer got the product.

	order_estimated_delivery_date: estimated delivery date of the products.
 
### The reviews.csv contain following features:
	review_id: Id of the review given on the product ordered by the order id.

	order_id: A unique id of order made by the consumers.

	review_score: review score given by the customer for each order on the scale of 1–5.

	review_comment_title: Title of the review.

	review_comment_message: Review comments posted by the consumer for each order.

	review_creation_date: Timestamp of the review when it is created.

	review_answer_timestamp: Timestamp of the review answered.

### The products.csv contain following features:
	product_id: A unique identifier for the proposed project.

	product_category_name: Name of the product category.

	product_name_length: length of the string which specifies the name given to the products ordered.

	product_description_length: length of the description written for each product ordered on the site.

	product_photos_qty: Number of photos of each product ordered available on the shopping portal.

	product_weight_g: Weight of the products ordered in grams.

	product_length_cm: Length of the products ordered in centimeters.

	product_height_cm: Height of the products ordered in centimeters.

	product_width_cm: width of the product ordered in centimeters.

## Key Highlights:
	Import the dataset and do usual exploratory analysis steps like checking the structure & characteristics of the dataset:
1.	Data type of all columns in the "customers" table.
2.	Get the time range between which the orders were placed.
3.	Count the Cities & States of customers who ordered during the given period.
 
	In-depth Exploration:
1.	Is there a growing trend in the no. of orders placed over the past years?
2.	Can we see some kind of monthly seasonality in terms of the no. of orders being placed?
3.	During what time of the day, do the Brazilian customers mostly place their orders? (Dawn, Morning, Afternoon or Night)
1.	0-6 hrs : Dawn
2.	7-12 hrs : Mornings
3.	13-18 hrs : Afternoon
4.	19-23 hrs : Night

	Evolution of E-commerce orders in the Brazil region:
1.	Get the month-on-month no. of orders placed in each state.
2.	How are the customers distributed across all the states?
	Impact on Economy: Analyze the money movement by e-commerce by looking at order prices, freight and others.
1.	Get the % increase in the cost of orders from year 2017 to 2018 (include months between Jan to Aug
only).
You can use the "payment_value" column in the payments table to get the cost of orders.
2.	Calculate the Total & Average value of order price for each state.
3.	Calculate the Total & Average value of order freight for each state.

 

	Analysis based on sales, freight and delivery time.
1.	Find the no. of days taken to deliver each order from the order’s purchase date as delivery time. Also, calculate the difference (in days) between the estimated & actual delivery date of an order. Do this in a single query.

You can calculate the delivery time and the difference between the estimated & actual delivery date using the given
formula:
1.	time_to_deliver = order_delivered_customer_date - order_purchase_timestamp
2.	diff_estimated_delivery = order_estimated_delivery_date - order_delivered_customer_date
2.	Find out the top 5 states with the highest & lowest average freight value.
3.	Find out the top 5 states with the highest & lowest average delivery time.
4.	Find out the top 5 states where the order delivery is really fast as compared to the estimated date of delivery. You can use the difference between the averages of actual & estimated delivery date to figure out how fast the delivery was for each state.
	Analysis based on the payments:
1.	Find the month-on-month no. of orders placed using different payment types.
2.	Find the no. of orders placed on the basis of the payment installments that have been paid.


 ## Insights:
 	We have 99441 customers in our dataset.
 	We have 96096 number of Unique Customers ids.
 	Customers belong to 14994 different locations.
 
 	Customers are from different 4119 cities and 27 states from Brazil.
 
 	There are 8011 cities and 27 states in our dataset.
 
 	Total sellers are 3095, who are from 611 different cities and 23 states in Brazil and from 2246 different locations as per zip-code.
 
 	Time range for which the data is given is 25 months i.e., from 2016 to 2018.
 
 	compare to 2017, revenue has increased in 2018 by 20%.
 
 	Average number of orders are higher during November, average orders are comparatively low in September and October month. May, July and August have higher average orders compare to other months.
 
 	Monday, Tuesday and Wednesdays have comparatively higher number of orders.
 
 	Most of the customers prefer to order during afternoon followed by night .
 
 	The orders are low from 12am. To 6 am.
 
 	we can observe the trend of increasing orders with time and also for revenue.
 
 	The number of orders has been increased by 136% from 2016 to 2017 and by 20% from 2017 to 2018.
 
 	The revenue has been increased by 123% from 2016 to 2017 and by 20% from 2017 to 2018.
 
 	The growth rate for November is highest!
 
 	The growth rate for July and August in 2017 and 2018 is comparatively very low!
 
 	In the month of May, July, August the average number of orders are also high compared to other months.
 
 	There is an increase in the cost of orders in Feb, Mar of 2017 and Jan of 2018 during the months from January and August.
 
 	There are 32951 different products and 73 different product categories.
 
 	PCs , HOUSE PASTALS OVEN AND CAFÉ, Argo industry and ELECTRICS 2 are having highest average product price categories.
 
 	The bed table bath, HEALTH BEAUTY, sport leisure, computer accessories, Furniture Decoration, housewares are the top
 selling product categories. 
 
 	The orders and revenues are high in the state SP(Sao Paulo) , RJ(Rio De Janeiro) and MG(Minas Gerais) compared to other states.
 
 	The states RR, PB, RO, AC, PI are having highest average freight values. And these states also produce low revenues.
 
 	The states SP, PR, MG, RJ, DF are having lowest average freight values. And these states also produce higher revenues.
 
 	The states RR, AP, AM, AL, PA are having highest delivery time. And these states also produce lower revenues.
 
 	The states SP, PR, MG, DF, SC are having lower average delivery time. And these states also produce higher revenues.
 
 	The average delivery time and freight value are directly proportional to each other.
 
 	Highest payment have been done through credit card and then UPI.
 
 
 ## Recommendations:
 	Though there is an increasing trend in the orders and revenue over the time period, but to increase the sales during low
 selling months like Jan, Apr, June, Sept and Oct, company can provide some kind of discounts .
 
 	The average delivery time should be reduced to increase the number of orders .
 
 	The delivery time can be reduced by reducing the approval time .
 
 	The north and northeast region of Brazil have high freight value and high delivery time. It should be reduced.
 
 	Adding more products in the top selling categories can increase the revenue .
