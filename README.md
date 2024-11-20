# Power BI Portfolio

# Superstore Sales Dashboard

### Project Overview

This project focuses on creating a comprehensive Sales Dashboard in Power BI. The goal was to analyze sales data, derive insights, and visualize performance metrics. Key steps included data transformation, the use of DAX formulas, and creating interactive reports. 


### Objectives

- Analyze overall sales performance and profitability trends.
- Examine regional, category, and segment-wise performance.
- Provide actionable insights and recommendations.


### Process Summary

- Step 1 : Load data into Power BI Desktop, dataset is a Excel file.
- Step 2 : Open power query editor & in View tab under Data Preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : It was observed that the headers were in the first row, and they were changed to column headers in the Transform tab under 'Use First Row as Headers' and also checked the Data Type were correct.
- Step 4 : Finally, the Close & Apply tab was used once the data was ready for further analysis.
- Step 5 : In the Table View, changed the format of the "Order Date" and "Ship Date" columns using the Column Tools tab under the Formatting section.

        The format was updated to "14-03-2001 (dd-mm-yyyy)"

  
- Step 6 : Extracted Month, Quarter, and Year from the Order Date column by right-clicking on it and creating new columns using DAX formulas:

         Order Month = Orders[Order Date].[Month]          
         Order Quarter = Orders[Order Date].[Quarter]
         Order Year = Orders[Order Date].[Year]
 


- Step 7 : Created a new column named as "Day of Week" using the 'WEEKDAY' DAX function to determine the day of the week the order was placed: 

        Day of Week = WEEKDAY(Orders[Order Date], 2)


- Step 8 :  Created a new column named "Weekday/Weekend" using the 'IF function' to identify whether the order was placed on a weekday or a weekend:

       Weekday/Weekend = IF(Orders[Day of Week] = 6 || Orders[Day of Week] = 7, "Weekend", "Weekday") 


- Step 9 : Created a new column named "Days for Shipment" using the 'DATEDIFF' DAX function to calculate the total number of days it took for product shipment:

      Days for Shipment = DATEDIFF(Orders[Order Date], Orders[Ship Date], DAY)

- Step 10 : Added a currency symbol for the Sales column using the "Column Tools" tab under the Formatting section. The format was set to Currency, and decimal places were adjusted to 2 points.
           
- Step 11: In the Report View, created a Title using the"Text Box" option in the Home tab and formatted it as required.

- Step 12 : Created three reports for the Sales Dashboard:

  (a) Overall Sales

  (b) State and Region Level Analysis
  
  (c) Category and Sub-Category Level Analysis
  
   
- Step 13 : In the Overall Sales Report, the following visualizations were created:

  (a) Three Cards: Total Sales, Total Profit, and Total Quantity Sold

  ![Card1](https://github.com/user-attachments/assets/6a94de40-a8e2-4460-a767-cbbfcc2408c7)

  ![Card2](https://github.com/user-attachments/assets/f0426780-4d4a-44ab-be61-08402d1a3dfb)

   ![Card 3](https://github.com/user-attachments/assets/7d9c872d-247f-477d-92fe-fec02fd93539)

 
  (b) Slicer: Order Date

   ![Slicer 1](https://github.com/user-attachments/assets/4dbc8dff-5625-4cee-a720-f511e798f689)
 
  (c) Line and Stacked Column Chart: Sales and Profit by Year

  (d) Donut Chart: Sales and Profit by Segment

  (e) Pie Chart: Sales and Profit by Category

  (f) Clustered Column Chart: Sales by Year and Quarter

  (g) Filled Map Chart: Sales by State



- Step 14 : In the "State and Region Level Analysis", the following visualizations were created:

   (a) Three Slicers: Region, State, and Order Year

   ![Slicer 2](https://github.com/user-attachments/assets/47396280-9b2f-4f52-8157-4fd194c2a45f)

  (b) Table Chart: Sales, Profit, and Quantity for each City

  (c) Clustered Bar Chart: Sales by State and Category

  (d) Area Chart: Profit by Year and Category

  (e) Line and Clustered Column Chart: Profit and Quantity by Category and Sub-Category

   (f) Funnel Chart: Sales by Segment

        
- Step 15 : In the "Category and Sub-category Level Analysis", the following visualizations were created:

  (a) Two Slicers: Category and Sub-Category

  ![Slicer 3](https://github.com/user-attachments/assets/45876034-dcaa-4267-8118-bd19f31deef2)


  (b) Treemap: Profit and Sales by Region and Segment

  (c) Donut Chart: Quantity and Sales by Segment

  (d) Scatter Chart: Sales, Quantity, and Profit by Sub-Category

  (e) Line Chart: Profit by Year and Quarter

  (f) Line Chart: Sales by Year and Quarter

 
 - Step 16 : The report was finally completed to publish in the Power BI Service.
 
 
 # Report Snapshot (Power BI DESKTOP)

 ![Report 1](https://github.com/user-attachments/assets/df037f6f-95a7-4e91-9b2b-cfac50b64c2a)


 ![Report 2](https://github.com/user-attachments/assets/dcef0de5-bb28-4330-9390-403dee3ba6b3)

 
![Report 3](https://github.com/user-attachments/assets/a04b8248-caee-4524-a572-7a12799bed8d)


# Insights

A three page report was created on Power BI Desktop

Following inferences can be drawn from the dashboard;


### 1. Overall Sales Performance:

- Total Sales: $1.71M, Profit: $216.92K, Quantity: 28K.

- Declining profit in 2017 despite stable sales indicates rising costs or pricing issues.


### 2. Segments & Categories:


- Consumer segment leads in sales (52%) and profit; Corporate and Home Office need growth strategies.

- Technology Category dominates sales but has a small margin. Furniture shows losses despite high sales.

### 3. Regional Analysis:

- West and East regions outperform; Central and South require attention.

- Top-performing states: California, New York, and Texas.


### 4. Sub-Category Analysis:

- Accessories, Paper and Appliances perform well. 
- Losses in Furniture (especially Tables and Bookcases) need to be addressed.


### 5. Seasonal & Yearly Trends:

- Q4 has peak sales, indicating strong seasonal demand.

- Profit declined in 2017, requiring cost/pricing review.



## Recommendations:
- Focus on improving Furniture profitability.
- Boost performance in Central and South regions.
- Grow Corporate and Home Office segments.
- Maximize Q4 sales with promotions.
- Investigate profit decline in 2017 to optimize costs.


## Tools and Skills Demonstrated
- Tools: Power BI, DAX
- Skills: Data Modeling, Data Transformation, Interactive Visualizations


## Conclusion
This project highlights my ability to transform raw data into valuable insights through dynamic visualizations. It showcases expertise in Power BI, data modeling, and actionable decision-making tailored to business goals.
