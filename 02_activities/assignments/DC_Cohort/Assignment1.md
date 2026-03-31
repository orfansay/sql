# DC Assignment 1: Meet the farmersmarket.db and Basic SQL

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

#### Submission Parameters:
* Submission Due Date: `March 31, 2026`
* Weight: 30% of total grade
* The branch name for your repo should be: `assignment-one`
* What to submit for this assignment:
    * This markdown (Assignment1.md) with written responses in Section 4
    * One Entity-Relationship Diagram (preferably in a pdf, jpeg, png format).
    * One .sql file 
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pulls/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-one`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.

*** 

## Section 1:
You can start this section following *session 1*.

Steps to complete this part of the assignment:
- Load the farmersmarket.db and browse its content
- Create a logical data model

<br>
If this is your first time in DB Browser for SQLite, the following instructions may help:

#### 1) Load Database
- Open DB Browser for SQLite
- Go to File > Open Database
- Navigate to your farmersmarket.db 
	- This will be wherever you cloned the GH Repo (within the **05_src/sql** folder)
	- ![db_browser_for_sqlite_choose_db.png](./images/01_db_browser_for_sqlite_choose_db.png)

#### 2) Configure your windows
By default, DB Browser for SQLite has three windows, with four tabs in the main window and three tabs in the bottom right window
- Window 1: Main Window (Centre)
	- Stay in the Database Structure tab for now
- Window 2: Edit Database Cell (Top Right)
- Window 3: Remote (Bottom Right)
	- Switch this to DB Schema tab (very bottom)

Your screen should look like this (or very similar)
![db_browser_for_sqlite.png](./images/01_db_browser_for_sqlite.png)

#### 3) The farmersmarket.db
There are 10 tables in the Main Window:
1) booth
2) customer
3) customer_purchases
4) market_date_info
5) product
6) product_category
7) vendor
8) vendor_booth_assignments
9) vendor_inventory
10) postal_data

Switch to the Browse Data tab, booth is selected by default

<img src="./images/01_the_browse_data_tab.png" width="900">


Using the table drop down at the top left, explore some of the contents of the database

<img src="./images/01_the_table_drop_down_at_the_top_left.png" width="200">

Move on to the Logical Data Model task when you have looked through the tables


### Build Logical Data Model

Recall during session 1:

I diagramed the following four tables:
- product
- product_category
- vendor
- vendor_inventory

 <img src="./images/01_farmers_market_logical_model_partial.png" width="500">


#### Prompt 1:
Choose two tables and create a logical data model. There are lots of tools you can do this (including drawing this by hand), but I'd recommend [Draw.io](https://www.drawio.com/) or [LucidChart](https://www.lucidchart.com/pages/). 

A logical data model must contain:
- table name
- column names
- relationship type

Please do not pick the exact same tables that I have already diagrammed. For example, you shouldn't diagram the relationship between `product` and `product_category`, but you could diagram `product` and `customer_purchases`.

**HINTS**:
- You will need to use the Browse Data tab in the main window to figure out the relationship types.
- You can't diagram tables that don't share a common column
	- These are the tables that are connected
	- <img src="./images/01_farmers_market_conceptual_model.png" width="600">
- The column names can be found in a few spots (DB Schema window in the bottom right, the Database Structure tab in the main window by expanding each table entry, at the top of the Browse Data tab in the main window)

https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=Logical_data_model.drawio&dark=auto#R%3Cmxfile%3E%3Cdiagram%20name%3D%22Page-1%22%20id%3D%22GVgULpFdwEyrME__LbBn%22%3E7VhLb9s4EP4tPQjoHgzoETv2sXHS7qJoGzTF9mgwIi0RoUiFpCJ7f%2F0ORdKSLMdW3GaBLXqwJc0MPw7n8ZFSkCyLzQeJyvyTwIQFcYg3QXIdxPFlnMC%2FEWytYDYLrSCTFFtR1Aru6D%2FECb1ZRTFRPUMtBNO07AtTwTlJdU%2BGpBR132wtWH%2FWEmVkILhLERtKv1OscyudT8NW%2FiehWe5njkKnKZA3dgKVIyzqjii5CZKlFELbu2KzJMzEzsfFjnv%2FjHbnmCRcjxlw%2FeXT9%2Bu%2Fv92pL9fk89e%2F3ovbx4%2BTKBzCOGSltz4ImmxAd1XnVJO7EqVGXEO6QZbrgsFTBLd22BNilRsWxDNmxqkS8R7g7LEyq75KYVY9SQUTMkjegYnM7t%2BCR0u49Zc%2FGuRwlNFacD1Zo4KyrTWd1OT%2BgeqJ0ohjJHHHzHljrLiQBWId3ROSFME1RabKDprULulGeQF%2BNBpGtCZyAutNKc%2BGI4Usc8QdZGxlJrYTxGjGrRhclbqjohw3mTG6sNx0NFoC1hrg%2FUScWG2Tp8aLAwusKW6aouNCLSTuO72byAewmVBpKR7IpLZ9MHQIk1RIpKng%2Bx6tmUB6X4ipKhlymaKcUVDE4RtalEJCvmwQfKnAXeauTU2ZJBysKZvchkeaJV44FwdAN3EwnweLG48InWNB%2BxOB2NavFzdFTiSsuNMuruU%2BEFEQLbdgkndY4cJ1Wd0yyKUTOZDkcmGfHU3GM8ebyPFXtkNuWxxuXJe%2FpOP7hInufZOPYoJMiqo80OhnBGVH8Z2oTKN%2BWBZhLyrRPHylqFyMD8rRqP53oYoWrxWLAzvLsZh1lnxig0CqtFv0mm4IPrRjLCulYRXSNx%2BmT77xUqdaralUesVRQTot2jE8NpahdigqjHv8XpX9bh8JVQpgarZK4cAzFuyMzO%2ByfCjzniteqxDiswtB1bRgqCH6Zj9z57rwmVNCECeR0bXpP6dJXtgjDu2r6XeeMbIHlwzhFn1ymk%2BPkxNicBjgSJMrUXGsBunYreP8DE3%2Fv7TlN75Xq97ZyBhMfz6N3VYyzZEiK3DwCIW02pO0U0qBq1S%2FZMhjBWcoqrfnUx0w3KrlO%2Fg9NmjjRhdIPhC9wlD%2FvwofXp5dUT%2FIh6vSFdRvYhyZKneaJnjwdv9yRiQcvzNfEuAphQOEommfD6RZhSGC5%2FJ5KkH%2BY4IkDN6envoed0%2FHp5N2K2jzXrQ53BpRtAehBFQWcaO6Hw%2F2gHY0%2FRwQVHVG9ADodD7hsf0GYs3bD0nJzb8%3D%3C%2Fdiagram%3E%3C%2Fmxfile%3E

***

## Section 2:
You can start this section following *session 2*.

Steps to complete this part of the assignment:
- Open the assignment1.sql file in DB Browser for SQLite:
	- from [Github](./02_activities/assignments/assignment1.sql)
	- or, from your local forked repository  
- Complete each question, by writing responses between the QUERY # and END QUERY blocks

### Write SQL

#### SELECT
1. Write a query that returns everything in the customer table.
2. Write a query that displays all of the columns and 10 rows from the customer table, sorted by customer_last_name, then customer_first_ name.

SELECT *
FROM customer;

SELECT *
FROM customer
ORDER BY customer_last_name, customer_first_name
LIMIT 10;

<div align="center">-</div>

#### WHERE
1. Write a query that returns all customer purchases of product IDs 4 and 9. Limit to 25 rows of output.
2. Write a query that returns all customer purchases and a new calculated column 'price' (quantity * cost_to_customer_per_qty), filtered by customer IDs between 8 and 10 (inclusive) using either:
	1.  two conditions using AND
	2.  one condition using BETWEEN
Limit to 25 rows of output.

SELECT *
FROM customer_purchases
WHERE product_id IN (4, 9);

SELECT *,
       quantity * cost_to_customer_per_qty AS price
FROM customer_purchases
WHERE customer_id BETWEEN 8 AND 10
LIMIT 25;

<div align="center">-</div>

#### CASE
1. Products can be sold by the individual unit or by bulk measures like lbs. or oz. Using the product table, write a query that outputs the `product_id` and `product_name` columns and add a column called `prod_qty_type_condensed` that displays the word “unit” if the `product_qty_type` is “unit,” and otherwise displays the word “bulk.”

SELECT product_id,
    product_name,
    CASE 
        WHEN product_qty_type = 'unit' THEN 'unit'
        ELSE 'bulk'
    END AS prod_qty_type_condensed
FROM product;

2. We want to flag all of the different types of pepper products that are sold at the market. Add a column to the previous query called `pepper_flag` that outputs a 1 if the product_name contains the word “pepper” (regardless of capitalization), and otherwise outputs 0.
SELECT product_id,
    product_name,
    CASE 
        WHEN product_qty_type = 'unit' THEN 'unit'
        ELSE 'bulk'
    END AS prod_qty_type_condensed,
    CASE 
        WHEN LOWER(product_name) LIKE '%pepper%' THEN 1
        ELSE 0
    END AS pepper_flag
FROM product;

<div align="center">-</div>

#### JOIN
1. Write a query that `INNER JOIN`s the `vendor` table to the `vendor_booth_assignments` table on the `vendor_id` field they both have in common, and sorts the result by `market_date` then `vendor_name`. Limit to 24 rows of output. 
SELECT *
FROM vendor
INNER JOIN vendor_booth_assignments
    ON vendor.vendor_id = vendor_booth_assignments.vendor_id
ORDER BY market_date, vendor_name
LIMIT 24;

***

## Section 3:
You can start this section following *session 3*.

Steps to complete this part of the assignment:
- Open the assignment1.sql file in DB Browser for SQLite:
	- from [Github](./02_activities/assignments/assignment1.sql)
	- or, from your local forked repository  
- Complete each question, by writing responses between the QUERY # and END QUERY blocks

### Write SQL

#### AGGREGATE
1. Write a query that determines how many times each vendor has rented a booth at the farmer’s market by counting the vendor booth assignments per `vendor_id`.
SELECT vendor_id,
       COUNT(*) AS booth_rental_count
FROM vendor_booth_assignments
GROUP BY vendor_id;
2. The Farmer’s Market Customer Appreciation Committee wants to give a bumper sticker to everyone who has ever spent more than $2000 at the market. Write a query that generates a list of customers for them to give stickers to, sorted by last name, then first name.

SELECT c.customer_id,
    c.customer_first_name,
    c.customer_last_name,
    SUM(cp.quantity * cp.cost_to_customer_per_qty) AS total_spent
FROM customer 
INNER JOIN customer_purchases 
    ON c.customer_id = cp.customer_id
GROUP BY c.customer_id, c.customer_first_name, c.customer_last_name
HAVING sum(cp.quantity * cp.cost_to_customer_per_qty) > 2000
ORDER BY c.customer_last_name, c.customer_first_name;

   
**HINT**: This query requires you to join two tables, use an aggregate function, and use the HAVING keyword.

<div align="center">-</div>

#### Temp Table
1. Insert the original vendor table into a temp.new_vendor and then add a 10th vendor: Thomass Superfood Store, a Fresh Focused store, owned by Thomas Rosenthal
   
**HINT**: This is two total queries -- first create the table from the original, then insert the new 10th vendor. When inserting the new vendor, you need to appropriately align the columns to be inserted (there are five columns to be inserted, I've given you the details, but not the syntax)

To insert the new row use VALUES, specifying the value you want for each column:  
`VALUES(col1,col2,col3,col4,col5)`

<div align="center">-</div>

#### Date
1. Get the customer_id, month, and year (in separate columns) of every purchase in the customer_purchases table.
   
**HINT**: you might need to search for strfrtime modifers sqlite on the web to know what the modifers for month and year are!

Limit to 25 rows of output. 

2. Using the previous query as a base, determine how much money each customer spent in April 2022. Remember that money spent is `quantity*cost_to_customer_per_qty`.
   
**HINTS**: you will need to AGGREGATE, GROUP BY, and filter...but remember, STRFTIME returns a STRING for your WHERE statement...
AND be sure you remove the LIMIT from the previous query before aggregating!! 

*** 

## Section 4:
You can start this section anytime.

Steps to complete this part of the assignment:
- Read the article
- Write, within this markdown file, between 250 and 1000 words. No additional citations/sources are required.

### Ethics

Read: Qadri, R. (2021, November 11). _When Databases Get to Define Family._  Wired. <br>
    https://www.wired.com/story/pakistan-digital-database-family-design/

Link if you encounter a paywall: https://archive.is/srKHV or https://web.archive.org/web/20240422105834/https://www.wired.com/story/pakistan-digital-database-family-design/

**What values systems are embedded in databases and data systems you encounter in your day-to-day life?**

Consider, for example, concepts of fariness, inequality, social structures, marginalization, intersection of technology and society, etc.


```
Your thoughts...
``` Databases and data systems are products of human beings and they are influenced by the values, culture, and worldviews of those who design develop them. In the case of states, they are influenced by the state ideology and priorities in addition to values of individuals involved in developing them. For instance, security has been one of the main priorities of Pakistani state since the establishment of the country and has influenced how they design and make use of databases and data systems. Moreover, Pakistan, for the most part, has been a conservative and traditional society, which influences how they define certain social phenomenon such as family and parenting. This, in turn, influence how information on family and parenting are gathered and documented in their databases. In other settings, certain other value systems are prevalent, which influences how databases are designed and governed. For instance, neoliberal values have become widespread in the last several decades, that emphasize efficiency, effectiveness and accountability. These values have not only influenced interactions among social systems but also the relationship between technology and society. For instance, when I came to Canada a few years ago and opened a bank account, they had to delete half of my first name because their database allowed a certain number of characters. One reason for this character limitation might be efficiency – taking a small space in the database and little time to type. I also experienced such character limitation in certain other databases and websites where I had to delete part of my first name so that they could process the application. To sum up, the power (those with power) determines how databases are designed, what types of information are collected, what format this information can take and what values drive these their governance. 
