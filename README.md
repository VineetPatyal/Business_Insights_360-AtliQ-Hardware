# Business_Insights_360-AtliQ-Hardware

## Project Overview

AtliQ Hardware is growing rapidly in the recent years, and they have decided to implement the data analytics using PowerBi in their company for the first time to surpass their competitors in the market and to make data driven decisions. This project is hoped to give answers to the questions of stakeholder in terms all the aspects like finance, sales, marketing and supply chain.

I worked on this project by following the Codebasics PowerBi Course, Link to the course is https://app.powerbi.com/links/pdBeHzIMu1?ctid=b33942ea-a291-45f0-ad5b-5130073d8a6b&pbi_source=linkShare

[Live Report Link](https://www.novypro.com/project/atliq-hardware-business-insights-360-15)

## Tech stacks

- SQL
- PowerBi Desktop
- Excel
- DAX language
- DAX studio (for optimizing the report)
- Project charter file

## PowerBI techniques Learnt

- What are all the questions should be asked before staring the project
- Creating calculated columns
- creating measure using DAX language
- Data modeling
- Using Bookmarks to switch between two visuals
- Page navigation with buttons
- Using divide function to prevent zero division errors
- creating date table using m language
- Dynamic titles based on the applied filters
- Using KPI indicators
- Conditional formatting the values in visuals using icons or background color
- Data validation techniques
- PowerBi services
- Publishing reports to PowerBi services
- Setting up personal gateway to set up the auto refresh of data
- PowerBi App creation
- Collaboration, workspace, access permissions in PowerBi services
- etc.


## Business related terms

- Gross price
- Pre-invoice deductions
- Post-Invoice deductions
- Net Invoice sale
- Gross Margin
- Net sales
- Net profit
- COGC - cost of goods sold
- YTD - Year to Date
- YTG - Year to Go
- Direct
- Retailer
- Distributors
- Consumer

## Company’s back ground

AltiQ hardware is a company which has grown vastly in the recent years, and opened business all over the globe. It is a company which sells, computer and computer accessories through three mediums/channel

- Retailers
- Direct
- Distributors

Recently the company has faced a unforeseen loss by opening store in America based on the surveys, intuition and some excel analysis and also the company’s competitors has handful of analytics team to perform analysis and make data driven decision. So, the AltiQ hardware has no other option other than building their analytics team for data driven insights and decisions in the future to survive better in the industry. 

Project kick off session, where you should get clear of for what and why this project and all other questions you have with regards to the project

### Questions to ask before starting with dashboard

- What is the objective of building this PowerBi dashboard?
- In what terms the success of this project will be measured?
- What will be time dead-line of the project?
- do the stakeholders expecting pre-view before the actual release?
- What are all the hopes stakeholders have out of this project?
- what are all fears the stakeholder have in terms of building this dashboard?
- Who are all will be using this dashboard and for what purpose?
- what are all expectation the stakeholders have, by the completion of this project?
- What can go wrong while building this project?
- what are all the resources/ data needed to build this dashboard?
- is there any inputs from stakeholders in terms of design and views of the dashboard?

After the project kick off meetings, the data engineering team has given the data as per the request of data analytics team, let’s explore them.

### Dataset **Understanding.**

Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get good understanding of what are data available.

Dimension table : It will have the static data like details of customer and products

Fact table : It will have the data about the transactions  

- gdb041:
    - dim_customer
        - **27** distinct markets (ex India, USA, spain)
        - **75** distinct customers thorough out the market
        - **2** types of platforms
            - Brick & Motors - Physical/offline store
            - E-commerce - Online Store (Amazon, flipkart)
        - Three channels
            - Retailer
            - Direct
            - Distributors
    - dim_market
        - **27** distinct markets (ex India, USA, spain)
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - nan
            - LATAM
    - dim_product
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
                - Networking
                - Storage
        - There are 14 different categories, Like Internal HDD, keyboard
        - There are different variants available for the same product
    - fact_forecast_monthly
        - This table is used to forecast the customer’s need in advance, which can help in
            - Higher customer satisfaction
            - Reduced cost in warehouses for storage purpose
        - The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
        - All the date of the month will be replaced by the start date of the month
        - It will have all the column names and in the end it will have the forecast quantity need of the customer
    - fact_sales_monthly
        - This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.
- gdb056
    - freight_cost
        - This table has details of travel cost and other cost for each market with fiscal year
    - gross_price
        - Has the details of gross prices with product code
    - manufacturing_cost
        - Has the details of manufacturing cost with product code with year
    - Pre_invoice_dedutions
        - Has the details of pre invoice deductions percentage for each cutomer with year
    - Post_invoice_deductions
        - Post invoice deductions and other deductions details

# Data Model

Data modeling plays a vital role and is considered as the basement of report. All the visuals will be build upon the data model.
Poor data modeling affects the over all performance of the report.
Following Good practices of data modeling is must. Refer this page to get to know the good practices Blog
In this project, we have followed Snowfall data modeling method.

Snap of a data model

![data modelling](https://github.com/VineetPatyal/Business_Insights_360-AtliQ-Hardware/assets/152878178/f68e8f02-cdcc-46d5-a877-fd905c80d5e9)

## Importing data into PowerBi

- As the database is MySQL in this project, we need to import the datasets from Mysql database to PowerBi by providing the Database access credential

### Dashboard designing

Based on the mock ups received as requirement, the team will start designing the visuals and create measure as and when required

## Home view

In Home view, all the views button will be available. User will land on specific view page by clicking the button 

- Infopage
- Finance View
- Sales View
- Marketing View
- Supply chain View
- Executive View
- Product Sales view
- Support

# Snapshot of a Infopage

![Infopage](https://github.com/VineetPatyal/Business_Insights_360-AtliQ-Hardware/assets/152878178/dede30f1-b1fb-4360-8529-30f7f3da7f5d)

#Snapshot of Finance View

![Finance View](https://github.com/VineetPatyal/Business_Insights_360-AtliQ-Hardware/assets/152878178/e2ab1fd0-3d12-4675-9d8f-17829c0243ab)

#Snapshot of Sales View

![Sales View](https://github.com/VineetPatyal/Business_Insights_360-AtliQ-Hardware/assets/152878178/4bc27374-97ed-432f-8127-2acdb7f4f475)

#Snapshot of Marketing View

![Marketing View](https://github.com/VineetPatyal/Business_Insights_360-AtliQ-Hardware/assets/152878178/8f2bd611-230b-4d9b-966e-110fd48b4697)

#Snapshot of Supplychain view

![Supply chain view](https://github.com/VineetPatyal/Business_Insights_360-AtliQ-Hardware/assets/152878178/c82c4470-1b62-4727-b5ed-3246e646ba9c)

#Snapshot of Executive View

![Executive View](https://github.com/VineetPatyal/Business_Insights_360-AtliQ-Hardware/assets/152878178/e57e8b23-9868-43b2-ab81-c5cfa16f0d3f)

#Snapshot of Product Sales View

![Product Sales View](https://github.com/VineetPatyal/Business_Insights_360-AtliQ-Hardware/assets/152878178/bf7d9579-8002-47b1-a301-1d9e9c22b7b8)

