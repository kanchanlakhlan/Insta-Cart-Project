# Insta-Cart-Project

The dataset for this project is a relational set of files describing customers' orders over time. The goal of the project is to predict which products will be in a user's next order. 

The dataset is anonymized and contains a sample of over 3 million grocery orders from more than 200,000 Instacart users. For each user, we are provided between 4 and 100 of their orders, with the sequence of products purchased in each order. We are also provided the week and hour of day the order was placed, and a relative measure of time between orders.

# File descriptions
1. aisles.csv
 aisle_id, aisle  
 1, prepared soups salads  
 2, specialty cheeses  
 3, energy granola bars 
 
2. departments.csv
 department_id,department  
 1,frozen  
 2,other  
 3,bakery 
 
 3. order_products__*.csv
These files specify which products were purchased in each order. order_products__prior.csv contains previous order contents for all customers. 'reordered' indicates that the customer has a previous order that contains the product. Note that some orders will have no reordered items. You may predict an explicit 'None' value for orders with no reordered items. See the evaluation page for full details.

     order_id,product_id,add_to_cart_order,reordered  
     1,49302,1,1  
    1,11109,2,1  
    1,10246,3,0  
 
 4. orders.csv
This file tells to which set (prior, train, test) an order belongs. You are predicting reordered items only for the test set orders. 'order_dow' is the day of week.

     order_id,user_id,eval_set,order_number,order_dow,order_hour_of_day,days_since_prior_order  
     2539329,1,prior,1,2,08,  
     2398795,1,prior,2,3,07,15.0  
     473747,1,prior,3,3,12,21.0 
 
 5. products.csv
 product_id,product_name,aisle_id,department_id
 1,Chocolate Sandwich Cookies,61,19  
 2,All-Seasons Salt,104,13  
 3,Robust Golden Unsweetened Oolong Tea,94,7  
 
