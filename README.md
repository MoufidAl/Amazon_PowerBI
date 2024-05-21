# Amazon_PowerBI
A Power BI dashboard analyzing sales, deliveries, prices and more.

-----------
## Notes on the project.
Amazon Fashion Table

1.	In the amazon fashion table, we see some errors in the “large” column where it contains more than one image link per cell.so we will fix that by splitting the column by a delimiter and removing the extra column.

2.	In the amazon fashion table,  we need to split the values in the “Category” column for a cleaner look. At first, we split this column by using the  “ lowercase to uppercase split” that way we have categories such as MensShoes become Mens  | Shoes. In their respective columns. Then in the second column, in this example the “Shoes” column we want to remove null values. So we replace Null. Next we combine the original split column back into one by creating a new one and adding them up together.

3.	Lastly, in the amazon fashion table we will remove any unnecessary columns that we created while cleaning as well as any columns that had no data in them. And we also filter the “large” column to remove any products that do not have a link.

Data Options Table
1.	Create a new table using the below script: 
Data_Options = 
DATATABLE("Type",STRING,
            "Name",STRING
                ,{
                    {"1","Sales"},
                    {"2","Units"}
                }
)


Amazon Sales Table
1.	When we open the table, we see most columns are named “Column 1, 2,3..etc” keeping them like this would be very confusing, unhelpful, and unprofressional so our first task is to clean the columns by renaming according to the date they contain. Luckily we had the headers in the first row so we clicked on “use first row as headers”.
Connections
1.	The amazon fashion table contains the sales prices for items listed however the amazon sales report contains the quantity sold for each item. Items are marked by their ASIN code thus I used the ASIN to merge the amazon sales report with the amazon fashion table in order to bring the price to the amazon sales reports.. 
2.	Now we take the newly added sale price and multiply it by the quantity column for each row giving us the total sales. 

3.	DATA MODEL:

a.	Connected tables using the ASIN column.
