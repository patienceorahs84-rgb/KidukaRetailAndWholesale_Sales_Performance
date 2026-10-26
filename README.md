# KidukaRetailAndWholesale_Sales_Performance
Tools Used 
* Microsoft Excel
* Power BI

  ## Project Overview
The project consists of different sheets such as customers,orders, orderdetails and products which are to be used to generate the profit margin, revenue, orders received and the stock available so as to ensure smooth  running of the business.Kiduka sells FMCG, electronics, beauty products, stationery and agro-inputs to shops and individuals across Uganda. Orders come in through four channels: Online, In-Store, WhatsApp and Phone Order. Payments are made by cash, mobile money, credit card or bank transfer.

I cleaned the raw Excel data in Power Query, built a data model, wrote DAX measures and designed a four-page report that answers practical business questions.

## Business Questions Answered
* How much revenue and profit did the business make, and at what margin?
* Which product categories, products and regions earn the most profit?
* Which products need restocking right now?
* How much money is tied up in stock that is not selling?
* How many orders are completed, pending or cancelled, and is the business reaching its completion target?

## Key Results
* Measure	                         Value
* Total Revenue:                   UGX 722.4M
* Total Cost:                      UGX 547.3M
* Gross Profit:	                   UGX 175.1M
* Profit Margin:                   24.2%
* Total Orders: 	                 950
* Order Completion Rate:           86.2% (target 90%)
* Products below reorder level:	   4 (target 0)
* Dead Stock Value:                UGX 18.07M

## Main Insights
* Electronics drives the business. It earns about UGX 105.7M in gross profit, roughly 60% of the total. Agriculture comes second with UGX 34.1M.
* The Central region leads in gross profit (UGX 56.9M), followed by Western (UGX 45.9M), Eastern (UGX 37.7M) and Northern (UGX 34.6M).
* The Itel A60 Smartphone is the most profitable product at UGX 33.8M, even though Samsung A05 and Tecno Spark Go bring in more revenue. Their lower margins leave them with about UGX 18M each.
* Four products are at or below their reorder level: one each in Electronics, Agriculture, Food Staples and Beverages. These need restocking immediately.
* Dead stock stands at UGX 18.07M, well above the target set in the report. Products with no sales in the last 14 days are counted as dead stock, and they tie up cash that could be used elsewhere.
* Order completion of 86.2% is below the 90% target, mainly because of 82 cancelled and 49 pending orders.

## Dashboard Pages
* Page 1: Executive Summary	Revenue, cost, gross profit, margin, and order status counts with completion rate
* Page 2: Profitability	Gross profit by category and region, plus a product table with revenue and profit
* Page 3: Inventory Health	Products below reorder level, dead stock vs target, inventory value by category and a stock table
* Page 4: Order Completion	Completed orders against the 90% target

  ## Data Cleaning (Power Query)
Table	                  
* Table_Products:	Extra spaces and inconsistent capital letters in text columns(Problem).	Trimmed text and applied Capitalize Each Word(Solution).
 Table_Products:	2 rows with a stock quantity of -1 "data entry error"(Problem).	Replaced with 0(Solution).
* Table_Orders:	4 duplicate rows(Problem).	Removed duplicates on OrderID(Solution).
  Table_Orders:	15 missing payment methods(Problem).	Replaced with "unknown"(Solution).
  Table_Orders:	No day or month fields for analysis(Problem).	Added Day Name and Month Name columns(Soluton)
* Table_Customers:	3 missing districts(Problem).	Replaced with "Unknown"(Solution)
All tables	Columns loaded with the wrong data types were	Set to correct types (text, date, whole number, decimal)
