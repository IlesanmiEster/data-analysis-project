# data-analysis-project
A project to give insight into a company sale. Providing a quarterly report with all the key metrics, to access the health of the business and make the necessary decisions.


create database project;
use project;
select * from new_wheels_sales_qtr_1;
select * from new_wheels_sales_qtr_2;
select * from new_wheels_sales_qtr_3;
select * from new_wheels_sales_qtr_4;
create table temp_t(shipper_id int,
shipper_name text, 
shipper_contact_details text, 
product_id int, 
vehicle_maker text,
vehicle_model text, 
vehicle_color text,
vehicle_model_year int, 
vehicle_price double, 
quantity int,
discount double,
customer_id text, 
customer_name text, 
gender text,
job_title text, 
phone_number text, 
email_address text, 
city text,
country text, 
state text, 
customer_address text,
order_date text,
order_id text,
ship_date text,
ship_mode text, 
shipping text, 
postal_code int,
credit_card_type text,
credit_card_number double,
customer_feedback text, 
quarter_number int);

insert into temp_t(shipper_id,
shipper_name, 
shipper_contact_details, 
product_id, 
vehicle_maker,
vehicle_model, 
vehicle_color,
vehicle_model_year, 
vehicle_price, 
quantity,
discount,
customer_id, 
customer_name, 
gender,
job_title, 
phone_number, 
email_address, 
city,
country, 
state, 
customer_address,
order_date,
order_id,
ship_date,
ship_mode, 
shipping, 
postal_code,
credit_card_type,
credit_card_number,
customer_feedback, 
quarter_number)
select shipper_id,
shipper_name, 
shipper_contact_details, 
product_id, 
vehicle_maker,
vehicle_model, 
vehicle_color,
vehicle_model_year, 
vehicle_price, 
quantity,
discount,
customer_id, 
customer_name, 
gender,
job_title, 
phone_number, 
email_address, 
city,
country, 
state, 
customer_address,
order_date,
order_id,
ship_date,
ship_mode, 
shipping, 
postal_code,
credit_card_type,
credit_card_number,
customer_feedback, 
quarter_number from new_wheels_sales_qtr_1; 
insert into temp_t(shipper_id,
shipper_name, 
shipper_contact_details, 
product_id, 
vehicle_maker,
vehicle_model, 
vehicle_color,
vehicle_model_year, 
vehicle_price, 
quantity,
discount,
customer_id, 
customer_name, 
gender,
job_title, 
phone_number, 
email_address, 
city,
country, 
state, 
customer_address,
order_date,
order_id,
ship_date,
ship_mode, 
shipping, 
postal_code,
credit_card_type,
credit_card_number,
customer_feedback, 
quarter_number)
select shipper_id,
shipper_name, 
shipper_contact_details, 
product_id, 
vehicle_maker,
vehicle_model, 
vehicle_color,
vehicle_model_year, 
vehicle_price, 
quantity,
discount,
customer_id, 
customer_name, 
gender,
job_title, 
phone_number, 
email_address, 
city,
country, 
state, 
customer_address,
order_date,
order_id,
ship_date,
ship_mode, 
shipping, 
postal_code,
credit_card_type,
credit_card_number,
customer_feedback, 
quarter_number from new_wheels_sales_qtr_2; 

insert into temp_t(shipper_id,
shipper_name, 
shipper_contact_details, 
product_id, 
vehicle_maker,
vehicle_model, 
vehicle_color,
vehicle_model_year, 
vehicle_price, 
quantity,
discount,
customer_id, 
customer_name, 
gender,
job_title, 
phone_number, 
email_address, 
city,
country, 
state, 
customer_address,
order_date,
order_id,
ship_date,
ship_mode, 
shipping, 
postal_code,
credit_card_type,
credit_card_number,
customer_feedback, 
quarter_number)
select shipper_id,
shipper_name, 
shipper_contact_details, 
product_id, 
vehicle_maker,
vehicle_model, 
vehicle_color,
vehicle_model_year, 
vehicle_price, 
quantity,
discount,
customer_id, 
customer_name, 
gender,
job_title, 
phone_number, 
email_address, 
city,
country, 
state, 
customer_address,
order_date,
order_id,
ship_date,
ship_mode, 
shipping, 
postal_code,
credit_card_type,
credit_card_number,
customer_feedback, 
quarter_number from new_wheels_sales_qtr_3; 

insert into temp_t(shipper_id,
shipper_name, 
shipper_contact_details, 
product_id, 
vehicle_maker,
vehicle_model, 
vehicle_color,
vehicle_model_year, 
vehicle_price, 
quantity,
discount,
customer_id, 
customer_name, 
gender,
job_title, 
phone_number, 
email_address, 
city,
country, 
state, 
customer_address,
order_date,
order_id,
ship_date,
ship_mode, 
shipping, 
postal_code,
credit_card_type,
credit_card_number,
customer_feedback, 
quarter_number)
select shipper_id,
shipper_name, 
shipper_contact_details, 
product_id, 
vehicle_maker,
vehicle_model, 
vehicle_color,
vehicle_model_year, 
vehicle_price, 
quantity,
discount,
customer_id, 
customer_name, 
gender,
job_title, 
phone_number, 
email_address, 
city,
country, 
state, 
customer_address,
order_date,
order_id,
ship_date,
ship_mode, 
shipping, 
postal_code,
credit_card_type,
credit_card_number,
customer_feedback, 
quarter_number from new_wheels_sales_qtr_4; 

select * from temp_t; -- verify data

DELIMITER //
create procedure vehicles_p()
begin
select *from temp_t;
end //

DELIMITER ;

-- Create the vehicles_t Table
CREATE TABLE vehicles_t (
    shipper_id int,
shipper_name text, 
shipper_contact_details text, 
product_id int, 
vehicle_maker text,
vehicle_model text, 
vehicle_color text,
vehicle_model_year int, 
vehicle_price double, 
quantity int,
discount double,
customer_id text, 
customer_name text, 
gender text,
job_title text, 
phone_number text, 
email_address text, 
city text,
country text, 
state text, 
customer_address text,
order_date text,
order_id text,
ship_date text,
ship_mode text, 
shipping text, 
postal_code int,
credit_card_type text,
credit_card_number double,
customer_feedback text, 
quarter_number int
);

-- Call the vehicle_p Stored Procedure to Retrieve Data
CALL vehicles_p;

-- Insert the Retrieved Data into the vehicle_t Table
INSERT INTO vehicles_t (shipper_id,
shipper_name, 
shipper_contact_details, 
product_id, 
vehicle_maker,
vehicle_model, 
vehicle_color,
vehicle_model_year, 
vehicle_price, 
quantity,
discount,
customer_id, 
customer_name, 
gender,
job_title, 
phone_number, 
email_address, 
city,
country, 
state, 
customer_address,
order_date,
order_id,
ship_date,
ship_mode, 
shipping, 
postal_code,
credit_card_type,
credit_card_number,
customer_feedback, 
quarter_number)
SELECT shipper_id,
shipper_name, 
shipper_contact_details, 
product_id, 
vehicle_maker,
vehicle_model, 
vehicle_color,
vehicle_model_year, 
vehicle_price, 
quantity,
discount,
customer_id, 
customer_name, 
gender,
job_title, 
phone_number, 
email_address, 
city,
country, 
state, 
customer_address,
order_date,
order_id,
ship_date,
ship_mode, 
shipping, 
postal_code,
credit_card_type,
credit_card_number,
customer_feedback, 
quarter_number FROM temp_t;

DELIMITER //
create procedure order_p()
begin
select 
order_id,
customer_id, 
shipper_id,
product_id,
quantity,
vehicle_price, 
order_date, 
ship_date,
discount,
ship_mode,
shipping, 
customer_feedback, 
quarter_number from vehicles_t;
end //
DELIMITER ;

DELIMITER //
create procedure customer_p()
begin
select 
customer_id, 
customer_name, 
gender,
job_title, 
phone_number, 
email_address, 
city,
country, 
state, 
customer_address,
postal_code,
credit_card_type,
credit_card_number from vehicles_t;
end //
DELIMITER ;

DELIMITER //
create procedure shipper_p()
begin
select shipper_id , 
shipper_name, shipper_contact_details from vehicles_t;
end //
DELIMITER ;

DELIMITER //
create procedure product_p()
begin
select product_id, vehicle_maker, 
vehicle_model, 
vehicle_color, 
vehicle_model_year, 
vehicle_price from vehicles_t;
end //
DELIMITER ;


CREATE TABLE order_t (order_id VARCHAR(100) PRIMARY KEY, 
customer_id text, 
shipper_id int,
product_id int,
quantity int,
vehicle_price double, 
order_date text, 
ship_date text,
discount double,
ship_mode text,
shipping text, 
customer_feedback text, 
quarter_number int);
-- Call the order_p Stored Procedure to Retrieve Data
CALL order_p;

-- Insert the Retrieved Data into the order_t Table
INSERT INTO order_t (order_id,
customer_id, 
shipper_id,
product_id,
quantity,
vehicle_price, 
order_date, 
ship_date,
discount,
ship_mode,
shipping, 
customer_feedback, 
quarter_number)
SELECT order_id,
customer_id, 
shipper_id,
product_id,
quantity,
vehicle_price, 
order_date, 
ship_date,
discount,
ship_mode,
shipping, 
customer_feedback, 
quarter_number
FROM vehicles_t;



CREATE TABLE customer_t (
customer_id VARCHAR(100) PRIMARY KEY,
customer_name text,
gender text, 
job_title text,
phone_number text, 
email_address text, 
city text,
country text, 
state text,
customer_address text,
postal_code int,
credit_card_type text,
credit_card_number double); 

-- Call the customer_p Stored Procedure to Retrieve Data
CALL customer_p;

-- Insert the Retrieved Data into the order_t Table
INSERT INTO customer_t (customer_id, 
customer_name,
gender, 
job_title,
phone_number, 
email_address, 
city,
country, 
state,
customer_address,
postal_code,
credit_card_type,
credit_card_number)
select customer_id, 
customer_name,
gender, 
job_title,
phone_number, 
email_address, 
city,
country, 
state,
customer_address,
postal_code,
credit_card_type,
credit_card_number FROM vehicles_t;




CREATE TABLE shipper_t (
shipper_id INT PRIMARY KEY,
shipper_name text, 
shipper_contact_details text );

-- Call the customer_p Stored Procedure to Retrieve Data
CALL shipper_p;

-- Insert the Retrieved Data into the order_t Table
INSERT INTO shipper_t (
shipper_id,
shipper_name, 
shipper_contact_details)
select shipper_id,
shipper_name, 
shipper_contact_details FROM vehicles_t;


CREATE TABLE product_t (
product_id INT PRIMARY KEY, 
vehicle_maker text, 
vehicle_model text, 
vehicle_color text, 
vehicle_model_year int,
vehicle_price double );

-- Call the customer_p Stored Procedure to Retrieve Data
CALL product_p;

-- Insert the Retrieved Data into the order_t Table
INSERT INTO product_t (
product_id,
vehicle_maker, 
vehicle_model, 
vehicle_color, 
vehicle_model_year,
vehicle_price)
select product_id, 
vehicle_maker, 
vehicle_model, 
vehicle_color, 
vehicle_model_year,
vehicle_price FROM vehicles_t;

TRUNCATE TABLE temp_t;
    
    SHOW COLUMNS FROM customer_t;



    CREATE VIEW veh_ord_cust_v AS
    SELECT
        o.order_id,
        o.customer_id AS order_customer_id,
        o.shipper_id,
        o.product_id,
        o.quantity,
        o.vehicle_price,
        o.order_date,
        o.ship_date,
        o.discount,
        o.ship_mode,
        o.shipping,
        o.customer_feedback,
        o.quarter_number,
        c.customer_id,
        c.customer_name,
        c.gender,
        c.job_title,
        c.phone_number,
        c.email_address,
        c.city,
        c.country,
        c.state,
        c.customer_address,
        c.postal_code,
        c.credit_card_type,
        c.credit_card_number
    FROM order_t o, customer_t c;
    
    
    # INNER JOIN customer_t c ON o.order_id = c.customer_id;
    
 CREATE VIEW veh_prod_cust_v AS
	SELECT  c.customer_id,
        c.customer_name,
        c.gender,
        c.job_title,
        c.phone_number,
        c.email_address,
        c.city,
        c.country,
        c.state,
        c.customer_address,
        c.postal_code,
        c.credit_card_type,
        c.credit_card_number,
        o.order_id,
        o.customer_feedback,
        p.product_id,
        p.vehicle_maker,
        p.vehicle_model,
        p.vehicle_color,
        p.vehicle_model_year,
        p.vehicle_price
		FROM order_t o, customer_t c, product_t p
        
        
	-- Create the function calc_revenue_f


DELIMITER $$

CREATE FUNCTION calc_revenue_f (quantity INT, vehicle_price DECIMAL(10,2), discount DECIMAL(10,2))
RETURNS DECIMAL(10,2)
DETERMINISTIC  
BEGIN  	
    DECLARE discounted_price DECIMAL(10,2);
    DECLARE revenue DECIMAL(10,2);
    
    -- Calculate the discounted price
    SET discounted_price = vehicle_price * discount;
    
    -- Calculate revenue as Quantity multiplied by Discounted Price
    SET revenue = quantity * discounted_price;
    
    -- Return the calculated revenue
    RETURN revenue;
END $$
DELIMITER ;


-- Create the function days_to_ship_f

DELIMITER $$
CREATE FUNCTION days_to_ship_f (order_date TEXT, ship_date TEXT)
RETURNS INT
DETERMINISTIC  
BEGIN  	
    DECLARE days_diff INT;
    
    -- Calculate the difference in days between order date and ship date
    SET days_diff = DATEDIFF(ship_date, order_date);
    
    -- Return the calculated difference in days
    RETURN days_diff;
END $$
DELIMITER ;

     
    -- --[Q1] What is the distribution of customers across states? Hint: For each state, count the number of customers.
select state, COUNT(*) AS customer_dist
FROM veh_ord_cust_v
GROUP BY state
ORDER BY state ASC;


SELECT COUNT(customer_id) AS Number_of_customers, state FROM vehicles_t
GROUP BY state;

-- Q2 What is the average rating in each quarter?
-- Very Bad is 1, Bad is 2, Okay is 3, Good is 4, Very Good is 5.

select quarter_number, AVG(CASE 
WHEN customer_feedback ='very bad' Then 1
WHEN customer_feedback ='bad' Then 2
WHEN customer_feedback = 'okay' Then 3
WHEN customer_feedback ='good' Then 4
WHEN customer_feedback = 'very good' Then 5
END) AS avg_rating
FROM veh_ord_cust_v
GROUP BY quarter_number;

WITH RatingNumbers AS (
    SELECT 
        CASE 
            WHEN customer_feedback = 'Very Bad' THEN 1
            WHEN customer_feedback = 'Bad' THEN 2
            WHEN customer_feedback = 'Okay' THEN 3
            WHEN customer_feedback = 'Good' THEN 4
            WHEN customer_feedback = 'Very Good' THEN 5
        END AS Rating_number,
        quarter_number
    FROM order_t
)
SELECT 
    quarter_number,
    AVG(Rating_number) AS average_rating
FROM RatingNumbers
GROUP BY quarter_number;

/* [Q3] Are customers getting more dissatisfied over time?

Hint: Need the percentage of different types of customer feedback in each quarter. Use a common table expression and
	  determine the number of customer feedback in each category as well as the total number of customer feedback in each quarter.
	  Now use that common table expression to find out the percentage of different types of customer feedback in each quarter.
      Eg: (total number of very good feedback/total customer feedback)* 100 gives you the percentage of very good feedback.*/
     
     WITH FeedbackCounts AS (
    SELECT 
        quarter_number,
        COUNT(*) AS total_feedback,
        SUM(CASE WHEN customer_feedback = 'Very Bad' THEN 1 ELSE 0 END) AS very_bad_count,
        SUM(CASE WHEN customer_feedback = 'Bad' THEN 1 ELSE 0 END) AS bad_count,
        SUM(CASE WHEN customer_feedback = 'Okay' THEN 1 ELSE 0 END) AS okay_count,
        SUM(CASE WHEN customer_feedback = 'Good' THEN 1 ELSE 0 END) AS good_count,
        SUM(CASE WHEN customer_feedback = 'Very Good' THEN 1 ELSE 0 END) AS very_good_count
    FROM order_t
    GROUP BY quarter_number
)
SELECT 
    quarter_number,
    total_feedback,
    very_bad_count,
    bad_count,
    okay_count,
    good_count,
    very_good_count,
    (very_bad_count * 100.0 / total_feedback) AS percentage_very_bad,
    (bad_count * 100.0 / total_feedback) AS percentage_bad,
    (okay_count * 100.0 / total_feedback) AS percentage_okay,
    (good_count * 100.0 / total_feedback) AS percentage_good,
    (very_good_count * 100.0 / total_feedback) AS percentage_very_good
FROM FeedbackCounts
ORDER BY quarter_number ASC;



/*[Q4] Which are the top 5 vehicle makers preferred by the customer.

Hint: For each vehicle make what is the count of the customers.*/

select vehicle_maker, COUNT(*) AS Top_vehicle_makers
FROM product_t
GROUP BY vehicle_maker 
ORDER BY COUNT(*) DESC
LIMIT 5;


/*[Q5] What is the most preferred vehicle make in each state?

Hint: Use the window function RANK() to rank based on the count of customers for each state and vehicle maker. 
After ranking, take the vehicle maker whose rank is 1.*/



WITH RankedVehicleMakes AS (
    SELECT 
        c.state,
        p.vehicle_maker,
        COUNT(*) AS customer_count,
        RANK() OVER (PARTITION BY c.state ORDER BY COUNT(*) DESC) AS maker_rank
    FROM product_t p
    JOIN order_t o ON p.product_id = o.product_id
    JOIN customer_t c ON o.customer_id = c.customer_id
    GROUP BY c.state, p.vehicle_maker
)
SELECT 
    state,
    vehicle_maker
FROM RankedVehicleMakes
WHERE maker_rank = 1;



/*[Q6] What is the trend of number of orders by quarters?

Hint: Count the number of orders for each quarter.*/



SELECT quarter_number, COUNT(quantity) AS Trend_order
FROM order_t
GROUP BY quarter_number 
ORDER BY quarter_number ASC;


/* [Q7] What is the quarter over quarter % change in revenue? 

Hint: Quarter over Quarter percentage change in revenue means what is the change in revenue from the subsequent quarter to the previous quarter in percentage.
      To calculate you need to use the common table expression to find out the sum of revenue for each quarter.
      Then use that CTE along with the LAG function to calculate the QoQ percentage change in revenue.*/

WITH QuarterlyRevenue AS (
    SELECT
        quarter_number,
        SUM(quantity * (vehicle_price * discount)) AS total_revenue
    FROM
        order_t
    GROUP BY
        quarter_number
)
SELECT
    qr.quarter_number,
    qr.total_revenue,
    LAG(qr.total_revenue) OVER (ORDER BY qr.quarter_number) AS previous_quarter_revenue,
    (qr.total_revenue - LAG(qr.total_revenue) OVER (ORDER BY qr.quarter_number)) / LAG(qr.total_revenue) OVER (ORDER BY qr.quarter_number) * 100 AS qoq_percentage_change
FROM
    QuarterlyRevenue qr
ORDER BY
    qr.quarter_number;


WITH QuarterlyRevenue AS (
    SELECT
        quarter_number,
        SUM(calc_revenue_f(quantity, vehicle_price, discount)) AS total_revenue
    FROM
        order_t
    GROUP BY
        quarter_number
	
)
SELECT
    qr.quarter_number,
    qr.total_revenue,
    LAG(qr.total_revenue) OVER (ORDER BY qr.quarter_number) AS previous_quarter_revenue,
    (qr.total_revenue - LAG(qr.total_revenue) OVER (ORDER BY qr.quarter_number)) / LAG(qr.total_revenue) OVER (ORDER BY qr.quarter_number) * 100 AS qoq_percentage_change
FROM
    QuarterlyRevenue qr
ORDER BY
    qr.quarter_number;



/* [Q8] What is the trend of revenue and orders by quarters?

Hint: Find out the sum of revenue and count the number of orders for each quarter.*/

SELECT quarter_number, COUNT(*) AS Total_Orders, SUM(calc_revenue_f(quantity, vehicle_price, discount)) AS total_revenue  
FROM order_t
GROUP BY quarter_number 
ORDER BY quarter_number ASC;

/*
    [Q9] What is the average discount offered for different types of credit cards?

Hint: Find out the average of discount for each credit card type.*/

SELECT
    c.credit_card_type,
    AVG(o.discount) AS average_discount
FROM
    order_t o
JOIN
    customer_t c ON o.customer_id = c.customer_id
GROUP BY
    c.credit_card_type;


/* [Q10] What is the average time taken to ship the placed orders for each quarters?
   Use days_to_ship_f function to compute the time taken to ship the orders.

Hint: For each quarter, find out the average of the function that you created to calculate the difference between the ship date and the order date.*/

SELECT quarter_number, AVG(days_to_ship_f(order_date, ship_date)) AS Shipping_time  
FROM order_t
GROUP BY quarter_number 
ORDER BY quarter_number ASC;




