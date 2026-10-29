# Mini-project-
** Retail Sales Data Analytics and Business Intelligence Dashboard **
1.	Imported the dataset into Excel power query
   
i)	Open excel
ii)	Imported the CSV (Go to Data → Get Data → From File → From Text/CSV.)
iii)	Clicked on transform data

2.	identify the missing value
I.	clicked on the filter checked the missing value 
3.	Replace blank values in Item
i)	Selected the Item column
ii)	Go to Transform → Replace Values
iii)	In the dialog box, enter: - Value to Find: Leave it empty. Replace With: Unknown
iv)	OK

 4.Standardize the text columns for category, item, payment method, location
  i)	Transform>format>trim
 5. replaced null value in quantity with median
6.Handle missing value in price per unit 
ii)	Custom column new column name as price cleaned.to calculate the missing price using total spent /quantity where both values are available.
iii)	If(price per unit) =null and (total spent) <> null and (quantity)<>null and (quantity)<>0 then ( total spent)/(quantity) else (price per unit)

7. Handling missing quantity
(1)	Add column> custom column new column named quantity cleaned 
ii)	If(quantity) =null and (total spent) <> null and (price cleaned )<>null and (price cleaned)<>0 then ( total spent)/( price cleaned) else (quantity)

8. Handling missing total spent
i)	Add column> custom column new column named total spent cleaned 
ii)	If(total spent) =null then if  (price cleaned) <> null and (quantity cleaned )<>null then ( price cleaned) *(quantity cleaned) else (total spent)

9.Removed the  original price per unit, quantity and total spent column and renamed the price cleaned to price per unit quantity cleaned to quantity, total spent cleaned to total spent.

10. added new column named discount applied cleaned  and replaced null value with” Unknown” and removed the discount applied column
 
 11. selected the transaction date column and right clicked  on it use locale given the data type as date and locale as English India

                 Power BI

      1.	Loaded the data. I imported the retail sales table into Power BI Desktop and reviewed the columns: Transaction ID, Customer ID, Transaction Date, Category, Item, Location, Payment Method, Quantity, Price per unit, Discount applied, and Total spent.
         
    2.	Prepared the data. I checked data types, removed duplicates, and handled blank values in Power Query.
    
3.	Created DAX measures. I built measures for Total Sales, Total Transactions, Average Spending, Total Quantity sold, and a Sales target for the gauge.
   
4.	Built the Dashboard page. I designed a banner and added four KPI cards, a yearly sales trend line, a sales-by-category bar chart, a payment method donut, a treemap, and a sales target gauge. I added slicers for Category, Location, and Payment Method.
   
5.	Analyzed spending drivers with Key Influencers. I explained average Total spent using Category, Location, Payment Method, Discount applied, and Item. The analysis showed that individual items, not category or payment method, drive spending per transaction.
   
6.	Wrote the Narrative page. I added a Total Sales by Category chart with an automatic narrative and edited the text into clear business insights. Butchers was the top category (about 13.3% of sales), and Milk Products was the lowest.
   
7.	Explored sales with the Decomposition Tree. I broke Total Sales down by Category, Item, Location, and Payment Method to see which segments contribute most.
   
8.	Analyzed the sales trend. I added a year-by-month matrix, a sales-by-year chart, and a waterfall of each year’s contribution. I found that yearly sales were stable (541K, 516K, 554K), that January was the peak month every year, and that 2025 has only partial data.
   
9.	Summarized and recommended. I wrote a Summary page with key findings and recommendations: plan promotions around January, promote the lowest category, investigate the 2023 dip, push high-value items, and refresh the report when 2025 data is complete.
    
10.	Connected the pages. I added navigation buttons so the report flows from Dashboard through each page to Summary and back, and checked that all pages share a consistent look.
    


