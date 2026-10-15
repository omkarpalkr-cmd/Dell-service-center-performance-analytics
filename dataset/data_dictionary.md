## Data Dictionary — Dell Service Center Performance Dashboard

# 1. Project Overview
The Dell Service Center Performance & SLA Analytics Dashboard is an interactive Power BI business intelligence project designed to analyze service operations, service-level agreement (SLA) compliance, technician productivity, customer satisfaction, product performance, and financial performance

## Tools Used: Power BI, Power Query, DAX

# 2. Column Definitions

|  # | Column                        | Data Type | Purpose                            |
| -: | ----------------------------- | --------- | ---------------------------------- |
|  1 | `AccID`                       | VARCHAR   | Account/service-center ID          |
|  2 | `Managers_Name`               | VARCHAR   | Service center manager             |
|  3 | `State`                       | VARCHAR   | State                              |
|  4 | `Region`                      | VARCHAR   | North/South/East/West              |
|  5 | `Technician`                  | VARCHAR   | Assigned technician                |
|  6 | `Purchase`                    | INT       | Units/products handled             |
|  7 | `Service`                     | INT       | Services completed                 |
|  8 | `Target`                      | DECIMAL   | Service/revenue target             |
|  9 | `Target_Achieved`             | DECIMAL   | Actual achievement                 |
| 10 | `Achieve_Percentage`          | DECIMAL   | Achievement %                      |
| 11 | `Service_Request_ID`          | VARCHAR   | Unique service request             |
| 12 | `Request_Date`                | DATE      | Service request date               |
| 13 | `Service_Date`                | DATE      | Actual service date                |
| 14 | `Closure_Date`                | DATE      | Ticket closure date                |
| 15 | `Product_Category`            | VARCHAR   | Laptop/Desktop/Monitor/Server/etc. |
| 16 | `Product_Model`               | VARCHAR   | Product model                      |
| 17 | `Serial_Number`               | VARCHAR   | Device serial number               |
| 18 | `Service_Type`                | VARCHAR   | Repair/Installation/Maintenance    |
| 19 | `Issue_Category`              | VARCHAR   | Hardware/Software/Network/etc.     |
| 20 | `Issue_Type`                  | VARCHAR   | Specific issue                     |
| 21 | `Priority`                    | VARCHAR   | Low/Medium/High/Critical           |
| 22 | `Warranty_Status`             | VARCHAR   | In Warranty/Out of Warranty        |
| 23 | `Warranty_Type`               | VARCHAR   | Standard/Extended/Premium          |
| 24 | `SLA_Hours`                   | INT       | Required resolution time           |
| 25 | `Resolution_Hours`            | DECIMAL   | Actual resolution time             |
| 26 | `SLA_Status`                  | VARCHAR   | Met/Breached                       |
| 27 | `First_Response_Hours`        | DECIMAL   | Time to first response             |
| 28 | `First_Time_Fix`              | TINYINT   | 1 = fixed on first visit           |
| 29 | `Repeat_Visit`                | TINYINT   | 1 = repeat visit required          |
| 30 | `Parts_Required`              | TINYINT   | Whether parts were required        |
| 31 | `Parts_Cost`                  | DECIMAL   | Replacement parts cost             |
| 32 | `Labor_Cost`                  | DECIMAL   | Technician labor cost              |
| 33 | `Total_Service_Cost`          | DECIMAL   | Parts + labor                      |
| 34 | `Customer_Rating`             | DECIMAL   | Customer rating, e.g. 1–5          |
| 35 | `CSAT_Score`                  | DECIMAL   | Customer satisfaction score        |
| 36 | `Customer_Feedback`           | VARCHAR   | Feedback category                  |
| 37 | `Escalation_Flag`             | TINYINT   | 1 = escalated                      |
| 38 | `Escalation_Reason`           | VARCHAR   | Reason for escalation              |
| 39 | `Service_Status`              | VARCHAR   | Open/In Progress/Resolved/Closed   |
| 40 | `Cancellation_Flag`           | TINYINT   | 1 = cancelled                      |
| 41 | `Cancellation_Reason`         | VARCHAR   | Reason for cancellation            |
| 42 | `Technician_Skill`            | VARCHAR   | Basic/Intermediate/Expert          |
| 43 | `Technician_Experience_Years` | DECIMAL   | Technician experience              |
| 44 | `Technician_Utilization`      | DECIMAL   | Technician utilization %           |
| 45 | `Daily_Service_Capacity`      | INT       | Expected daily capacity            |
| 46 | `Actual_Service_Count`        | INT       | Actual services handled            |
| 47 | `Revenue`                     | DECIMAL   | Service revenue                    |
| 48 | `Parts_Revenue`               | DECIMAL   | Revenue from parts                 |
| 49 | `Total_Revenue`               | DECIMAL   | Total service revenue              |
| 50 | `Profit_Margin`               | DECIMAL   | Profit margin %                    |
| 51 | `Complaint_Flag`              | TINYINT   | 1 = complaint raised               |
| 52 | `Complaint_Type`              | VARCHAR   | Service/Technician/Delay/etc.      |
| 53 | `Service_Channel`             | VARCHAR   | Call/Web/App/Walk-in               |
| 54 | `Customer_Type`               | VARCHAR   | Individual/Business/Enterprise     |
| 55 | `Created_Date`                | DATE      | Record creation                    |
| 56 | `Last_Updated_Date`           | DATE      | Last update                        |

# Table Fact_Service
Service_Request_ID
Technician_ID
Product_ID
Customer_ID
Location_ID
Date_ID
Request_Date
Service_Date
Closure_Date
Service_Status
Resolution_Hours
SLA_Hours
First_Time_Fix
Repeat_Visit
Parts_Cost
Labor_Cost
Revenue
Customer_Rating
CSAT

# Table Dim_Technician
Technician_ID
Technician_Name
Manager
Skill_Level
Experience
Region
State
Employment_Status

# Table Dim_Product
Product_ID
Product_Category
Product_Model
Product_Family
Warranty_Type

# Table Dim_Location
Location_ID
AccID
State
Region
Service_Center
City

# Table Dim_Date
Date
Year
Quarter
Month
Month_Name
Week
Day
Day_Name

## Records
Fact_Service
100,000 – 250,000 rows

Customers
20,000 – 50,000 rows

Technicians
500 – 2,000 rows

Service Centers
100 – 500 rows

Products
100 – 1,000 rows

Date Dimension
1,000 – 3,000 rows

