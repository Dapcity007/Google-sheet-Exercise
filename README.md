# GOOGLE SPREADSHEETS EXERCISES

## Stationery Company Sales Data Query
---
## Overview
   ### This project demonstrates how to use Google Sheets' query functions to analyze sales data from a stationery company. The dataset includes columns such as Region, Sales Rep, Item, Order Date, Month, Year, GDS Order Date, and Sales.  We will explore various queries to filter and summarize the data effectively.
---
## Table of Contents
-  Introduction
-  Setup
-  Using the QUERY Function
-  Examples
-  Tips and Best Practices
-  Conclusion
---
## Introduction
   ### Analyzing sales data is crucial for any business. This project uses Google Sheets' powerful QUERY function to extract insights from sales records, helping the stationery company make data-driven decisions.
---
## Set Up
1) Access the Data: The dataset is available at the following link: [downlad here](https://docs.google.com/spreadsheets/d/1o5Q6FwJdYmyYnaeECoCrS0VZAbpYjkwSfv2jiWAjcZc/edit?gid=0#gid=0). Make a copy of the sheet to your Google Drive.

2) Review the Data: Familiarize yourself with the columns:
- Region: The geographical area of the sale.
- Sales Rep: The name of the sales representative.
- Item: The type of stationery item sold.
- Order Date: The date the order was placed.
- Month: The month the order was placed.
- Year: The year the order was placed.
- GDS Order Date: The date in GDS format.
- Sales: The total sales amount.
  
3) Access the Functions: Familiarize yourself with the QUERY function by typing =QUERY( into a cell to see its syntax).
---
## Using the QUERY Function
### The QUERY function allows you to perform various operations on your dataset, including filtering, sorting, and aggregating data. Its basic structure is:
=QUERY(data, query, [headers])
 - data: The range of cells containing your data.
 - query: The string that specifies what you want to retrieve.
 - headers: (optional) The number of header rows in your data
---
## Example  Queries
---
1) From Picture one!![ Google Spreadsheet picture one](https://github.com/user-attachments/assets/6a57d743-4a31-43e0-a271-0a6804fdb6c1)

 - To show regions and items with sales above 500:
   
   =QUERY(A:H,"SELECT A,C,H WHERE H>500",1)
 - To show month with sales less than 100:
   
   =QUERY(A:H,"SELECT E,H WHERE H<100",1)
 - To show salesrep of item "Pen" and "Binder":
   
   =QUERY(A:H,"SELECT B,C WHERE C= 'Pen' OR C= 'Binder'",1)
 - To show regions of items "Pen" and "Binder" in 2014:
   
    =QUERY(A:H,"SELECT A,C,F WHERE (C= 'Pen' or C= 'Binder') AND F =2014",1)
 - To show items with salesrep to include "AN":
   
   =QUERY( A:H,"SELECT B,C WHERE (B LIKE '%an%') ",1 )
 - To show the total sales, maximum sales, average sales and count order of dates:
   
   =QUERY(A:H, "SELECT SUM(H), COUNT(D),MAX (H),AVG(H)",1)
   
2) From Picture two ![S](https://github.com/user-attachments/assets/c6fcbd4a-4e26-4a92-bb46-48f88437d42a)
 - To show sales rep to include "R" for "East" and "Central" region:
   
   =QUERY(A:H, "SELECT A,B WHERE B LIKE 'R%'",1)
- To show order date to include "04" for the month of Jul and Dec:
  
  =QUERY(A:H, "SELECT C, D, E, F WHERE D LIKE '%4' AND (E = 'Jul' OR E = 'Dec') AND F = 2014", 1)
- To show "sales" and "region" for the year 2015:

  =QUERY(A:H,"SELECT A, F, H WHERE F=2015",1)
- To show top 10 sales with "region" and "salesrep":
  
  =QUERY(A:H, "SELECT A, B, F, H WHERE F = 2014 ORDER BY H DESC LIMIT 10", 1)

3) From Picture three ![T](https://github.com/user-attachments/assets/e8f876ef-f027-4cec-8bdb-65a1e80fd736)
 - To show sales in "East" and "Central" in 2014:
   
   =QUERY(A:H,"SELECT A, H,F WHERE(A='Central' OR A= 'East') AND F= 2014")
- To show sales for the mounth of "Aug" and "Sep" in 2014:
  
  =QUERY(A:H, "SELECT E, F, H WHERE (E = 'Aug' OR E = 'Sep') AND F = 2014", 1)
- To show sales of item "Pen" and "Binder" in 2015:
  
  =QUERY( A:H, "SELECT C ,H, F WHERE (C= 'Pen' or C= 'Binder') AND  F= 2015",1)
- To show sales for salesrep Richard in 2014:

  =QUERY(A:H,"SELECT B,F,H WHERE (B= 'Richard') AND F=2014 ORDER BY H DESC ")

## Tips and Best Practices
---
- Ensure your data is accurate for effective querying.
- Consider using named ranges for easier management.
- Combine QUERY with other functions like FILTER and SORT for advanced analysis.
  
## Conclusion
---
Using Google Sheets and its QUERY function, this project highlights how to analyze and visualize sales data for a stationery company. These insights can help inform business decisions and improve sales strategies.

