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
5.Handle missing value in price per unit 
ii)	Custom column new column name as price cleaned.to calculate the missing price using total spent /quantity where both values are available.
iii)	If(price per unit) =null and (total spent) <> null and (quantity)<>null and (quantity)<>0 then ( total spent)/(quantity) else (price per unit)
6. Handling missing quantity
(1)	Add column> custom column new column named quantity cleaned 
ii)	If(quantity) =null and (total spent) <> null and (price cleaned )<>null and (price cleaned)<>0 then ( total spent)/( price cleaned) else (quantity)
7. Handling missing total spent
i)	Add column> custom column new column named total spent cleaned 
ii)	If(total spent) =null then if  (price cleaned) <> null and (quantity cleaned )<>null then ( price cleaned) *(quantity cleaned) else (total spent)
8.Removed the  original price per unit, quantity and total spent column and renamed the price cleaned to price per unit quantity cleaned to quantity, total spent cleaned to total spent.
9. added new column named discount applied cleaned  and replaced null value with” Unknown” and removed the discount applied column
 10. selected the transaction date column and right clicked  on it use locale given the data type as date and locale as English India 
