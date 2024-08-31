# Sales-Insights-Dashboard-Using-MySQL-and-Power-BI
**Company Overview**:    
Atliq Hardware, a manufacturer and supplier of computer hardware and peripherals, serves clients such as Excel Stores, Nomad Stores, Surge Stores, and Electrical Sara Stores.    
![image](https://github.com/user-attachments/assets/f75d1b74-b047-41f8-b594-4ac07005bd9c)  

**Problem Statement**:    
The Sales Director struggles to obtain accurate and actionable sales insights from regional managers, who often provide sugar-coated reports or large, unmanageable Excel files.    

**Solution Approach**:   

**Data Management**:  
![image](https://github.com/user-attachments/assets/728ca56a-e6fc-4e63-a45b-02ea97efc20d)    
Sales invoices are copied into a **MySQL database** by the Falcons IT team.    
The Data Miners team extracts, transforms, and loads data into a Data Warehouse, avoiding direct queries on the OLTP system to prevent performance issues.    
For simplicity, this project bypasses the Data Warehouse, directly extracting five tables **from the MySQL database into Power BI**:    
> **Transactions Table** (150,283 rows)  
![image](https://github.com/user-attachments/assets/0bfb4dbe-fe02-4a69-9884-f4070b1a35c4)    
> **Products Table** (279 rows)    
![image](https://github.com/user-attachments/assets/bbab83a9-eb9b-4bb1-ad83-1db0c8038d56)    
> **Markets Table** (17 rows)      
![image](https://github.com/user-attachments/assets/9cc1b26a-f558-49fc-89b8-2e4ba09ff897)    
> **Dates Table**(1,126 rows)    
![image](https://github.com/user-attachments/assets/9d04fc24-0555-4304-8b46-0956eb0de9b8)    
> **Customers Table** (38 rows)    
![image](https://github.com/user-attachments/assets/3e03660d-b423-43f3-bb62-b1a7222eb18b)  

**Data Model Used**:    
![image](https://github.com/user-attachments/assets/5df74200-91fd-4337-b801-ceafdd5447d1)  

**Data Transformation**:    
> Removed non-Indian records from the Markets table.    
![image](https://github.com/user-attachments/assets/0db7f3e8-6185-47c0-98d7-46a7fbd9928e)    
> Filtered out transactions with a sales amount of ≤ 0.    
![image](https://github.com/user-attachments/assets/db778177-c8ba-4337-9314-00b5fdcb0010)    
> Normalized the sales amount to INR for consistency.    
![image](https://github.com/user-attachments/assets/121184d8-780e-4a82-bef2-8ce94bddf753)  
![image](https://github.com/user-attachments/assets/188a30e4-4dff-45c7-a663-7d8076878604)     

**Dashboard Creation**:    
**KPIs included**:    Total Revenue, Total Sales Quantity, Revenue by Region, Sales Quantity by Region, Top 5 Customers by Revenue, Top 5 Products by Revenue, and Revenue Trends.    
                      Implemented slicers for years and months for dynamic filtering.    

**Key Insights**:    
Total Revenue: ₹984.81 million.    
Total Quantity Sold: 2.43 million units.    
Top Regions: Delhi NCR, Mumbai, and Ahmedabad contribute 81.42% of total revenue.    
Top Customer: Electrical Sara Stores, contributing 42% of total revenue.    
