# Canteen-Automation-System
An intuitive university canteen database system designed to streamline food ordering, track order history, and ensure data integrity. It empowers customers with seamless self-service while giving cashiers and managers role-based tools to efficiently manage orders and financial operations.

**Features & Architecture**
**Role-Based Access Control:** Separate workflows for Managers, Staff/Cashiers, and Customers.
**Database Normalization:** Fully normalized up to 3rd Normal Form (3NF) to eliminate redundancy and partial/transitive dependencies.
**Comprehensive Analytics:** Automated SQL Queries for inventory management, sales tracking, and revenue reporting.
**Data Security & Integrity:** Built with primary-foreign key constraints, data dictionary standardization, and recommended database maintenance practices (Backup & Recovery, Compact & Repair).

**System Design & Diagrams**
**Context Diagram Of Canteen Automation System**
<p align="center">
  <img src="https://github.com/user-attachments/assets/d69192f7-3608-4de2-a505-3006654b4a86" width="600" alt="Context Diagram"/>
</p>

**Data Flow Diagram (Manager)**
<p align="center">
  <img src="https://github.com/user-attachments/assets/77a942e0-2fc7-4709-aec5-9e13bdbbd789" width="600" alt="Context Diagram"/>
</p>

**Data Flow Diagram (Staff)**
<p align="center">
  <img src="https://github.com/user-attachments/assets/7d288259-e717-48a2-8364-1da974279142" width="600" alt="Context Diagram"/>
</p>

**Data Flow Diagram (Customer)**
<p align="center">
  <img src="https://github.com/user-attachments/assets/57ed448a-39a5-46d1-bfe1-9002252096ad" width="600" alt="Context Diagram"/>
</p>

**ERD for the System**
<p align="center">
  <img src="https://github.com/user-attachments/assets/e2d08181-c872-41cb-83dc-b1a06a3b5045" width="600" alt="Context Diagram"/>
</p>

**Relational Database**
<p align="center">
  <img src="https://github.com/user-attachments/assets/9f6399a3-319d-4d01-aab6-acdb487da35e"/>
</p>

**Flow chart diagram (Manager Level)**
<p align="center">
  <img src="https://github.com/user-attachments/assets/b64b794d-0a9a-493d-b3c3-04c9891aa025"/>
</p>

**Flow chart diagram (Staff Level)**
<p align="center">
  <img src="https://github.com/user-attachments/assets/1d36e9ce-a0f0-49cd-aa7b-a240b010b8a6"/>
</p>

**Flow chart diagram (Customer Level)**
<p align="center">
  <img src="https://github.com/user-attachments/assets/8e60b6e9-98cd-465f-b5c8-b8fa227d8f0a"/>
</p>

**Normalization**
**Unnormalizaed Form**
<p align="center">
  <img src="https://github.com/user-attachments/assets/35f27712-190d-4374-8b20-8904dcd7b6ca"/>
</p>

**1NF**
<p align="center">
  <img src="https://github.com/user-attachments/assets/47f30a67-566c-422d-9835-2e420f39dad9"/>
</p>

**2NF**
<p align="center">
  <img src="https://github.com/user-attachments/assets/486f3ed6-55bc-491e-b231-c9d8da21f829"/>
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/b3374164-6a92-40d0-ae35-b66a99c6d660"/>
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/9f68ab2b-03af-4e84-bd8d-b2cd5f7d8856"/>
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/c4e23d4f-ec26-4a64-9d77-9e52ed1c293f"/>
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/ab6e16e4-7286-47e7-9b7c-0b3871501833"/>
</p>

**3NF**
<p align="center">
  <img src="https://github.com/user-attachments/assets/ca8e034b-0412-4d91-b277-a51fface0edb"/>
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/d6cd11ee-d634-4d4c-93a1-e92e340daf2f"/>
</p>

**BCNF**
<p align="center">
  <img src="https://github.com/user-attachments/assets/7409d778-dda9-438f-a007-af8f5ee23c79"/>
</p>

**Data Dictionary**
<p align="center">
  <img src="https://github.com/user-attachments/assets/638c3c88-0e83-408a-8bb2-6032f394fb21"/>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/b6d1526a-a7ad-438e-a393-17a68c0da0dc"/>
</p>

**Some Queries**
**Customer By Staff Report**
<p align="center">
  <img src="https://github.com/user-attachments/assets/4ffa1877-46e7-484b-ba5d-30c9a2c7559f"/>
</p>
SELECT 
    CanteenStaff.StaffID, 
    CanteenStaff.StaffName, 
    Order.CustomerID, 
    Customer.CustomerName, 
    Order.OrderDate, 
    Order.OrderID
FROM Customer 
INNER JOIN (CanteenStaff INNER JOIN [Order] ON CanteenStaff.StaffID = Order.StaffID) 
    ON Customer.CustomerID = Order.CustomerID
GROUP BY 
    CanteenStaff.StaffID, CanteenStaff.StaffName, Order.CustomerID, 
    Customer.CustomerName, Order.OrderDate, Order.OrderID;
	
**Menu By FoodType Report**
<p align="center">
  <img src="https://github.com/user-attachments/assets/2f040b65-8a41-47e7-b4c1-df6b6aab7c10"/>
</p>

**Total_Onhand By FoodType Report**
<p align="center">
  <img src="https://github.com/user-attachments/assets/2e174a60-29e6-4b95-ae46-82d7275192ad"/>
</p>

**Monthly Income Report**
<p align="center">
  <img src="https://github.com/user-attachments/assets/cad13236-db40-4cb2-85a6-6f6fdba03276"/>
</p>

**OrderHistory Report**
<p align="center">
  <img src="https://github.com/user-attachments/assets/362cc987-8b47-4e6e-bb16-959b930e61c4"/>
</p>

**About Database System Security**
	System security plays as an essential role in protecting sensitive data, detecting and responding to threads, preventing unauthorized access, maintaining data integrity and ensuring data availability. If there is no system security, the user's data is not safe and can be easily lost or destroyed.  System security is one of the most important database tools to protect against these negative effects. The most famous methods for database system security are Encryption password, Compact and Repair and Creating Backup. These are tried during assignment performing but it is not included in this paper.










