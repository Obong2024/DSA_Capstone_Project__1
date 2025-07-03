# DSA_Capstone_Project__1

# Case Study 2: Kultra Mega Stores Inventory

## 1. Company Overview. Company Overview

**Kultra Mega Stores (KMS)**, headquartered in Lagos, specialises in offi ce supplies and furniture. Its customer base includes individual consumers, small businesses (retail), and large corporate clients (wholesale) across Lagos, Nigeria.

You have been engaged as a Business Intelligence Analyst to support the Abuja division of KMS. The Business Manager has shared an Excel fi le containing order data from 2009 to 2012 and has requested that you analyze the data and present your key insights and fi ndings.

Apply your SQL skills from the DSA Data Analysis class and solve both case scenarios as shared in the document.

## Case Scenario I

1. Which product category had the highest sales?
2. What are the Top 3 and Bottom 3 regions in terms of sales?
3. What were the total sales of appliances in Ontario?
4. Advise the management of KMS on what to do to increase the revenue from the bottom 10 customers
5. KMS incurred the most shipping cost using which shipping method?

## Case Scenario IICase Scenario II

6. Who are the most valuable customers, and what products or services do they typically purchase?
7. Which small business customer had the highest sales?
8. Which Corporate Customer placed the most number of orders in 2009 – 2012?
9. Which consumer customer was the most profi table one?
10. Which customer returned items, and what segment do they belong to?
11. If the delivery truck is the most economical but the slowest shipping method and Express Air is the fastest but the most expensive one, do you think the company appropriately spent shipping costs based on the Order Priority? Explain your answer

**Note:** To address this projct I decided to **"rename KMS file as Capstone"**. So where ever you find Capstone note that it is used in place of KMS

## Question 1: Which product category had the highest sales?

## Syntax:

~~~ 
select Top 1 Product_Category, SUM (sales) AS Total_sales
from Capstone
Group By Product_Category
Order By Total_Sales Desc;

**Note:** To address this Question 2 different syntax is used. One to show Top 3 and the second to show Bottom 3 as shown below;

## Question 2: What are the Top 3 and Bottom 3 regions in terms of sales

## Syntax:
 
~~~
 Select Top 3 
 Region, SUM (Sales) As Total_Sales
 From Capstone 
 Group By Region 
 Order By Total_Sales Desc;

Select Top 3
Region, SUM (Sales) As Total_Sales
From Capstone 
Group By Region 
Order By Total_Sales Asc;

## Question 3: What were the total sales of appliances in Ontario?

## Syntax:

~~~
Select SUM(Sales) AS Total_Sales
FROM Capstone
WHERE Product_Sub_Category = 'Appliances'
  AND Region = 'Ontario';

## Question 4: Advise the management of KMS on what to do to increase the revenue from the bottom 10 customers?

## Syntax: 

 ~~~
  Select Top 10 
  Customer_Name, Sum(Sales) As Total_Sales
  From Capstone
  Group By Customer_Name
  Order By Total_Sales Asc;







