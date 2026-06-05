# Sales Analysis

End-to-end sales data analysis project using SQL Server, Power BI, and DAX.  
Dataset source: [Kaggle — Global Online Orders Dataset](https://www.kaggle.com/datasets/javierspdatabase/global-online-orders)


## Dataset

### categories
| Column | Type | Description |
|--------|------|-------------|
| CategoryID | INT | Primary key |
| CategoryName | VARCHAR | Name of the category |
| DescriptionText | TEXT | Category description |

### customers
| Column | Type | Description |
|--------|------|-------------|
| CustomerID | VARCHAR | Primary key |
| CustomerName | VARCHAR | Company or customer name |
| ContactName | VARCHAR | Contact person |
| Address | VARCHAR | Street address |
| City | VARCHAR | City |
| PostalCode | VARCHAR | Postal code |
| Country | VARCHAR | Country |

### employees
| Column | Type | Description |
|--------|------|-------------|
| EmployeeID | INT | Primary key |
| LastName | VARCHAR | Last name |
| FirstName | VARCHAR | First name |
| BirthDate | DATE | Date of birth |
| Photo | VARCHAR | Photo path |
| Notes | TEXT | Additional notes |

### orders
| Column | Type | Description |
|--------|------|-------------|
| OrderID | INT | Primary key |
| CustomerID | VARCHAR | FK → customers |
| EmployeeID | INT | FK → employees |
| OrderDate | DATE | Date of order |
| ShipperID | INT | FK → shippers |

### orderdetails
| Column | Type | Description |
|--------|------|-------------|
| OrderDetailID | INT | Primary key |
| OrderID | INT | FK → orders |
| ProductID | INT | FK → products |
| Quantity | INT | Quantity ordered |

### products
| Column | Type | Description |
|--------|------|-------------|
| ProductID | INT | Primary key |
| ProductName | VARCHAR | Name of the product |
| SupplierID | INT | FK → suppliers |
| CategoryID | INT | FK → categories |
| Unit | VARCHAR | Unit of measure |
| Price | DECIMAL | Unit price |

### shippers
| Column | Type | Description |
|--------|------|-------------|
| ShipperID | INT | Primary key |
| ShipperName | VARCHAR | Name of the shipper |
| Phone | VARCHAR | Contact phone |

### suppliers
| Column | Type | Description |
|--------|------|-------------|
| SupplierID | INT | Primary key |
| SupplierName | VARCHAR | Supplier company name |
| ContactName | VARCHAR | Contact person |
| Address | VARCHAR | Street address |
| City | VARCHAR | City |
| PostalCode | VARCHAR | Postal code |
| Country | VARCHAR | Country |
| Phone | VARCHAR | Contact phone |


## Data Model

- **Fact table** : `orderdetails`
- **Dimension tables** : `categories`, `customers`, `employees`, `orders`, `products`, `shippers`, `suppliers`


## ❓ Business Questions

1. Which customers generate the most revenue?
2. Which months are the most profitable?
3. Which product categories perform best?
4. How do sales evolve over time?
5. Which employee generates the most sales?
6. Which country generates the most revenue?
7. Which product sells the most in quantity?
8. Which shipper delivers the most orders?
9. What is the average basket per customer?
10. Which products have never been ordered?

---

## Stack

- **SQL Server** : Data storage & transformation
- **Power BI Desktop** : Data modeling & visualization
- **DAX** : KPIs & measures
- **Power Query** : Data cleaning & preparation


## Author

**Joséphin Sylvère ANDRIANALISOA**  
[LinkedIn](https://www.linkedin.com/in/josephin-sylvere/) · [GitHub](https://github.com/ANDRIANALISOA-sylvere)