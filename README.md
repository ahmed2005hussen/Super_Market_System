# 🛒 Market Management System

## 📋 Overview
This project is a comprehensive market management system implemented in Python. It provides a complete solution for inventory management, user authentication with role-based access, sales processing, and detailed monthly reporting. All data is efficiently stored in CSV files for simplicity and portability.

## 📁 Project Structure
```
Market Project/
│
├── 🐍 main.py                    # Main program entry with user login and menus
├── 📊 StockManager.py            # StockManager class - manages products and reports
├── 💰 Cashier.py                 # Cashier class - handles sales transactions
├── 📦 Inventory.py               # Inventory class - manages product CRUD in CSV
├── 🛍️ MarketSells.py             # Sales class - handles sales recording
├── 📈 BalanceSheet.py            # Reporting class - monthly sales & profit reports
├── ✍️ Signup.py                  # Signup class - handles new user registration
├── 🔐 login.py                   # Login function - authenticates user credentials
│
├── 🗂️ Data Base/                 # Folder containing CSV files:
│   ├── 📋 inventory.csv          # Product inventory data
│   ├── 🧾 sales.csv              # Sales records
│   └── 👥 users.csv              # User accounts data
│
└── 📖 README.md                  # This documentation file
```

## ✨ Features

### 🔑 1. User Authentication
- **Secure Login System**: Validates credentials against `users.csv`
- **Role-Based Access Control**: Two distinct user types:
  - **📊 Stock Manager**: Complete access to inventory management and comprehensive reporting
  - **💰 Cashier**: Specialized access for sales transactions and inventory updates

### 📊 2. Stock Manager Capabilities
- 📋 **Inventory Overview**: Display current stock levels and product details
- ➕ **Product Management**: Add new products to the system
- ✏️ **Product Editing**: Modify product details (name, price, quantity, profit margins)
- 🔍 **Smart Search**: Find products quickly by ID
- 🗑️ **Product Removal**: Delete discontinued or obsolete products
- 📈 **Advanced Reporting**: Generate detailed monthly sales and profit analysis

### 💰 3. Cashier Operations
- 👀 **Stock Visibility**: View all available in-stock products
- 🛒 **Sales Processing**: Record and process customer transactions
- 🔄 **Auto-Update**: Automatically adjust inventory levels after each sale
- 💾 **Transaction Logging**: Save comprehensive sales data including:
  - Total transaction value
  - Profit margins
  - Timestamp
  - Cashier identification

### ✍️ 4. User Registration
- 🆕 **New User Signup**: Register users with complete profile information
- ✅ **Duplicate Prevention**: Verify username availability before registration
- 📝 **Complete Profiles**: Capture username, password, name, age, role, and salary
- 💾 **Secure Storage**: Save new user data directly to `users.csv`

## 📊 Data Files Format

### 👥 users.csv
```csv
user_name,Password,Name,Age,Type,Salary
john_doe,secure123,John Doe,28,Stock Manager,6000
jane_smith,pass456,Jane Smith,25,Cashier,4500
```

### 📦 inventory.csv
```csv
product_ID,product_name,product_price,product_quantity,product_profit,product_category,total_price,total_profit
101,Orange Juice,10.50,150,3.00,Beverages,1575.00,450.00
102,Chocolate Bar,5.25,200,1.75,Confectionery,1050.00,350.00
```

### 🧾 sales.csv
```csv
sale_ID,product_ID,product_name,quantity_sold,total_price,total_profit,sale_date,NameCashier,Month
101-5-Ahmed,101,Orange Juice,5,52.50,15.00,2025-08-13 22:00:00,Ahmed,8
102-3-Sarah,102,Chocolate Bar,3,15.75,5.25,2025-08-13 15:30:00,Sarah,8
```

## 🚀 How to Run

1. **📂 Setup**: Ensure all `.py` files and the `Data Base` folder are in the same directory
2. **▶️ Launch**: Run `python main.py` from your terminal
3. **🎯 Choose Action**: Select from Login, Sign Up, or Exit options
4. **👤 Access Dashboard**: Based on your role, access Stock Manager or Cashier features
5. **📋 Navigate**: Follow the intuitive menu prompts to manage your operations

## 🔧 System Requirements
- 🐍 Python 3.x
- 📊 CSV file support
- 🖥️ Terminal/Command line access

## ⚠️ Important Notes
- 💾 **Data Persistence**: All information is stored in CSV files within the `Data Base` folder
- 📋 **File Integrity**: Ensure CSV files exist with correct headers before first run
- 📅 **Reporting Logic**: Monthly sales reports utilize the "Month" column in `sales.csv`
- 🔐 **Security**: Password input uses masked display for enhanced security
- 🔄 **Backup Recommended**: Regular backups of CSV files are advisable

## 💡 Sample Usage

### 📊 Adding a Product (Stock Manager)
```python
# Initialize and add new product
manager = StockManager()
manager.add_product()
```

### 💰 Processing a Sale (Cashier)
```python
# Handle customer transaction
cashier = Cashier()
cashier.sale()
```

### 📈 Generating Monthly Report (Stock Manager)
```python
# View comprehensive monthly analysis
manager = StockManager()
manager.balance()
```

## 🎯 Key Benefits
- ✅ **User-Friendly Interface**: Intuitive menu-driven navigation
- 🔒 **Secure Access**: Role-based permissions and password protection
- 📊 **Comprehensive Reporting**: Detailed sales and profit analytics
- 🔄 **Real-Time Updates**: Automatic inventory synchronization
- 📁 **Portable Data**: CSV-based storage for easy backup and transfer

## 🤝 Support & Contact
If you have any questions, suggestions, or need assistance with the system, feel free to reach out. We're here to help make your market management experience smooth and efficient!

---
