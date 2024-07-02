# Echoes of 2024 - Financial Chronicles

### Dashboard Preview
![Echoes of 2024 - Financial Chronicles](https://github.com/dishadey-github/echoes-of-2024-final-chronicles/assets/60807918/432dbf53-657a-40a9-8c1e-f5293dd34263)

#### Overview
This project analyzes the sales, profit, and tax data for Roads & Co. using the dataset provided. The dashboard visualizes key performance indicators (KPIs) and trends to offer insights into the company's financial performance in 2024.

#### Dataset
The dataset includes sales order details with columns:

SalesOrderNumber: Unique identifier for each sales order.\
SalesOrderLine: Line number for each item in the sales order.\
OrderDate: Date of the order.\
Year: Year of the order.\
Month: Month of the order.\
FirstName: Customer's first name.\
LastName: Customer's last name.
EmailAddress: Customer's email address.\
Item: Description of the item sold.\
Quantity: Quantity of the item sold.\
UnitPrice: Price per unit of the item.\
TaxAmount: Tax amount for the order.

### Data Processing
#### Data Loading:
The dataset was loaded in the Power Query Editor. The Excel file contains columns like SalesOrderNumber, SalesOrderLine, OrderDate, Year, Month, FirstName, LastName, EmailAddress, Item, Quantity, UnitPrice, and TaxAmount.

#### Data Cleaning:
Checked for missing values and handled any inconsistencies.
Converted OrderDate to datetime format for time series analysis.
Extracted Year and Month from OrderDate to facilitate monthly and yearly analysis.

#### Data Transformation: Custom Column
- SalePrice
```
[Quantity]*[UnitPrice]
```
- Tax
```
[Quantity]*[TaxAmount]
```
Profit
```
[SalePrice]-[Tax]
```
#### Aggregations and Summarizations:
Grouped data by Item to find the most and least sold products.
Aggregated sales data by month to observe sales trends.
Calculated cumulative sales and profit figures for overall performance metrics.

### Measure Table:
It contains various calculated measures used in the dashboard. The measure table has been created to fulfill the KPIs. Measure table consists of the following -

#### 1. Total Sale
Computed by summing the product of Quantity and UnitPrice across all orders.
```
Total Sale = SUM(transformed_data[SalePrice])
```
#### 2. Total Profit
Estimated by aggregating total sales and subtracting costs and taxes. This assumes detailed cost information was available.
```
Total Profit = SUM(transformed_data[Profit])
```
#### 3. Quantity Ordered
Summed the Quantity column to get the total number of items sold.
```
Quantity Ordered = SUM(transformed_data[Quantity])
```

### Key Performance Indicators (KPIs)

![image](https://github.com/dishadey-github/echoes-of-2024-final-chronicles/assets/60807918/218b07e8-8fb2-44ca-92dc-42db878d2a1d)

#### Total Sales
- Description:
This is the total revenue generated of all sales transactions over the period.
- Technical Details:
Aggregation: The sum of the Total Sales column.
Visualization: A summary card on the dashboard shows the total sales amount.
Insights: The total sales amount of $10.69M provides an overall measure of the company’s revenue generation capability.

#### Total Profit
- Description:
The net profit after deducting costs and taxes from the total sales.
- Technical Details:
Calculation: Total Profit = Total Sales - Total Cost - Total Tax.
Aggregation: Sum of the calculated profit for each order.
Visualization: A summary card on the dashboard displays the total profit amount.
Insights: The total profit of $9.84M indicates effective cost management and high-profit margins.
This represents the total profit after deducting costs and taxes.

#### Quantity Ordered
- Description:
This is the total number of items sold over the period.
- Technical Details:
Aggregation: Sum of the Quantity column.
Visualization: A summary card on the dashboard shows the total quantity ordered.
Insights: The total quantity of 28.78K items provides insight into sales volume and product turnover.

![image](https://github.com/dishadey-github/echoes-of-2024-final-chronicles/assets/60807918/7eb8aa9f-cbae-4fdd-be90-24d9540a898e)

#### Sales by Month
- Description:
This metric represents the total sales amount aggregated by each month of the year.
- Technical Details:
Data Grouping: The sales data is grouped by the Month column.
Aggregation: The sum of the Total Sales for each month is calculated.
Visualization: A line graph is used to display the total sales amount per month, highlighting trends and seasonal variations.
Insights: Peaks in sales, particularly in November and December, indicate high seasonal demand, possibly due to holidays and year-end sales.

![image](https://github.com/dishadey-github/echoes-of-2024-final-chronicles/assets/60807918/246f6a96-a9ae-4012-8a2b-bc0c551daff8)

#### Sales by Order Line
- Description:
This metric shows the total sales amount for each sales order line item.
- Technical Details:
Data Grouping: Grouped by SalesOrderNumber and SalesOrderLine.
Aggregation: Summed the Total Sales for each order line.
Visualization: A bar chart displays the total sales amount for each order line, making it easy to identify the largest individual sales.
Insights: The highest sale by order line is $10,220,641, indicating a significant transaction that might warrant further investigation for special promotions or bulk orders.

![image](https://github.com/dishadey-github/echoes-of-2024-final-chronicles/assets/60807918/cf3ce1a8-04cd-4c99-9192-e699ec5d3add)

#### Most Sold Products
- Description:
The product with the highest total sales amount.
Technical Details:
- Data Grouping: Grouped by the Item column.
Aggregation: Sum of the Total Sales for each product.
Identification: The product with the maximum total sales value.
Visualization: A bar chart shows the most sold products, highlighting their total sales amounts.
Insights: The Mountain-200 Black, 46, with sales of $7,187,987.58, is the top performer, suggesting strong customer preference and market demand.

#### Least Sold Products
- Description:
The product with the lowest total sales amount.
- Technical Details:
Data Grouping: Grouped by the Item column.
Aggregation: Sum of the Total Sales for each product.
Identification: The product with the minimum total sales value.
Visualization: A bar chart shows the least sold products, highlighting their total sales amounts.
Insights: The Racing Socks, M, with sales of $1,483.35, is the least performer, indicating low customer interest or market penetration.


#### Filters
The dashboard includes filters for:
- Item: Allows the user to filter data by specific products.
- Month: Enables viewing data for specific months.

### Business Analytics Insights
#### Sales Trends:
Sales show a steady increase throughout the year, peaking in the last two months.
November and December are the highest-grossing months, indicating a seasonal trend, possibly due to holiday shopping.

#### Product Performance:
The Mountain-200 series, particularly in Black and Silver, are the top performers.
Lower sales are observed for smaller items like Racing Socks, indicating a focus on higher-value items.

#### Customer Insights:
High repeat purchases for specific high-value items suggest strong customer loyalty.
Customer email data can be used for targeted marketing campaigns to boost sales further.

#### Profit Analysis:
High total profit relative to total sales indicates effective cost management and high-profit margins.

#### Tax Contributions:
Detailed tax amounts provide clarity on tax contributions per order, aiding in tax compliance and reporting.

## Echoes of 2024 - Financial Chronicles (with filters)
Filter 1
- Item - Road-250 Black, 58
- Month - Applicable for all the months

![Road-250 Black, 58](https://github.com/dishadey-github/echoes-of-2024-final-chronicles/assets/60807918/8336e811-76b8-4a5e-ad45-2cbd6863c63e)

Filter 2
- Item - Hitch Rack-4-Bike
- Month - Applicable for all the months

![Hitch Rack-4-Bike](https://github.com/dishadey-github/echoes-of-2024-final-chronicles/assets/60807918/d299b438-7ddf-4c28-a98c-b3b666499806)

Filter 3
- Item - Touring-1000 Blue, 50
- Month - Applicable for all the months

![Touring-1000 Blue, 50](https://github.com/dishadey-github/echoes-of-2024-final-chronicles/assets/60807918/0fa7558e-3d5d-42aa-af08-e91ad8e1d929)

Filter 4
- Item - Road-650 Black, 52
- Month - Applicable for all the months

![Road-650 Black, 52](https://github.com/dishadey-github/echoes-of-2024-final-chronicles/assets/60807918/828f91ca-8760-4f56-bb79-a36b1b1e2d02)


