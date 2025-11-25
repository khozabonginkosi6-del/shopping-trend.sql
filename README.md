📘 Advanced SQL on NULL Functions
📌 Overview
This project demonstrates advanced SQL techniques for handling NULL values in retail shopping trend data. The queries showcase:

Filtering missing values

Replacing NULLs with defaults using IFNULL

Classifying records with CASE

Aggregating and grouping with conditions

Business insights such as customer segmentation, purchase behavior, and review analysis

🛠️ Requirements
SQL-compatible database (Snowflake, BigQuery, PostgreSQL, MySQL, SQL Server, Oracle, etc.)

Dataset:

Code
MYDATABASE.PUBLIC.SHOPING_TREND_01
Example columns:

customer_id

size

purchase_amount

item_purchased

season

payment_method

promo_code_used

review_rating

shipping_type

location

color

previous_purchases

frequency_of_purchases

category

age

gender

📂 Queries
1. 🔎 Missing Size & Purchase > 50
Find customers with missing size but purchase amount greater than 50.

2. 📅 Purchases by Season (NULL → Unknown)
Group purchases by season, replacing NULLs with 'Unknown Season'.

3. 💳 Customers by Payment Method (NULL → Not Provided)
Count customers by payment method, treating NULLs as 'Not Provided'.

4. 🎟️ Missing Promo Code & Low Rating
Show customers with no promo code and review rating below 3.0.

5. 🚚 Average Purchase by Shipping Type (NULL → 0)
Group by shipping type and calculate average purchase amount, replacing NULLs with 0.

6. 📍 Purchases per Location (>5, Non-NULL Payment)
Show locations with more than 5 purchases and valid payment methods.

7. 💵 Spender Category (CASE + NULL Handling)
Classify customers as High, Medium, Low spenders using CASE and IFNULL.

8. 🎨 Customers with Color Not NULL & Previous Purchases NULL
Find customers with missing previous purchases but valid color.

9. 🔄 Group by Frequency of Purchases
Group records by frequency of purchases.

10. 🛍️ Purchases per Category (Exclude NULL)
Count purchases per category, excluding NULL categories.

11. 📍 Top 5 Locations by Purchase Amount
Return top 5 locations with highest purchase amounts, replacing NULLs with 0.

12. 🚻 Entries with NULL Color by Gender & Size
Group customers by gender and size, counting entries with NULL color.

13. 📦 Items with >3 NULL Shipping Type
Identify items purchased more than 3 times with NULL shipping type.

14. 💳 Payment Method with NULL Review Rating
Count customers per payment method with missing review ratings.

15. ⭐ Average Review Rating per Category (>3.5)
Group by category, calculate average review rating (NULL → 0), filter >3.5.

16. 🎨 Colors Missing in ≥2 Rows + Avg Age
List colors missing in at least 2 rows and average age of those customers.

17. 🚚 Delivery Speed Classification
Classify delivery speed as Fast, Slow, Other using CASE.

18. 🎟️ Promo Code = Yes & Purchase Amount NULL
Find customers with NULL purchase amount but promo code used = Yes.

19. 📍 Max Previous Purchases per Location (Avg Rating > 4.0)
Group by location, show max previous purchases (NULL → 0), filter avg rating > 4.0.

20. 🚚 NULL Shipping Type + Purchase Between 30–70
Find customers with NULL shipping type and purchase amount between 30–70.
