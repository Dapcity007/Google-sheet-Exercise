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
1) Access the Data: The dataset is available at the following link: Stationery Sales Data. Make a copy of the sheet to your Google Drive.

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
1) From Picture one![Googlesheet Exercise pics one](https://github.com/user-attachments/assets/e91b6e02-1168-47f5-854b-77c2ba549520)
 - To show regions and items with sales above 500:
   =QUERY(A:H,"SELECT A,C,H WHERE H>500",1)
 - To show month with sales less than 100:
   =QUERY(A:H,"SELECT E,H WHERE H<100",1)
 - To show salesrep of item "Pen" and "Binder":
   =QUERY(A:H,"SELECT B,C WHERE C= 'Pen' OR C= 'Binder'",1)
 - To show regions of items "Pen" and "Binder" in 2014
    =QUERY(A:H,"SELECT A,C,F WHERE (C= 'Pen' or C= 'Binder') AND F =2014",1)
 - To show items with salesrep to include "AN"
   =QUERY( A:H,"SELECT B,C WHERE (B LIKE '%an%') ",1 )
 - 

  
