# Sales_Insights_PowerBI
I have used Power-BI to visualize and analyze the trends of sales of a company. 

## MySQL queries to explore the data:

SELECT * FROM sales.customers;

select count(*) from sales.customers;

select * from sales.markets;
select zone,count(*) as Num_of_markets from sales.markets group by zone;

select count(*) from sales.products;
select * from sales.products;

select * from sales.transactions;

select * from sales.transactions where sales_amount<=0;

select * from sales.date;

select sales.date.year,sum(sales.transactions.sales_amount) as revenue from sales.transactions
inner join sales.date 
on sales.date.date = sales.transactions.order_date 
group by sales.date.year 
order by revenue desc;

select distinct sales.transactions.currency from sales.transactions;

select * from sales.products where product_code is null;


## Screenshots of sales insights Using Power-BI Dashboard:

![image](https://user-images.githubusercontent.com/56965636/168462970-a983d750-9c1b-4f7d-b34b-e0bd74c3bcbb.png)

![image](https://user-images.githubusercontent.com/56965636/168462978-5c16b22f-49df-43c2-9424-fd5c2e571b55.png)

![image](https://user-images.githubusercontent.com/56965636/168462990-3e98051e-80ee-46da-b61b-8aad4b7591b6.png)

