# StockFlow – Inventory Management System

## 1. Project Overview

StockFlow is a web-based Inventory Management System designed to help small businesses manage their inventory and daily operations efficiently.

The system provides a centralized platform to manage products, categories, purchases, sales, stock movements, customers, suppliers, and users.

Its main objective is to reduce manual inventory tracking, minimize stock-related errors, and provide accurate information about available stock and business transactions.

## 2. Project Objectives

- Maintain accurate and up-to-date inventory records.
- Simplify product, customer, and supplier management.
- Track purchases and sales in a centralized system.
- Automatically update stock when purchases are received and sales are completed.
- Prevent sales when sufficient stock is unavailable.
- Maintain a history of all stock movements.
- Provide a dashboard with important inventory and transaction information.
- Implement role-based access control for administrators and regular users.

## 3. User Roles

StockFlow supports two user roles:

### 3.1 Admin

The Admin has complete control over the system.

Permissions:
- Log in and log out.
- View and manage dashboard information.
- Add, view, edit, deactivate, and manage products.
- Manage product categories.
- Manage purchases and sales.
- Manage stock and stock adjustments.
- Manage customers and suppliers.
- Create, view, edit, activate, and deactivate users.
- Manage business settings.

### 3.2 Regular User

Regular users can perform routine inventory operations but cannot access administrative functions.

Permissions:
- Log in and log out.
- View dashboard information.
- View, add, and edit products.
- Manage purchases and sales.
- View and manage stock.
- Perform stock adjustments with a reason.
- Manage customers and suppliers.
- View transaction and stock movement history.

Restrictions:
- Cannot manage users.
- Cannot modify administrative settings.
- Cannot permanently delete products.
- Cannot access restricted administrative operations.

## 4. Functional Requirements

### FR-01: User Authentication and Authorization

- The system shall allow users to log in using their email and password.
- Passwords shall be stored securely using hashing.
- The system shall support Admin and Regular User roles.
- The system shall restrict access to features based on user roles.
- The Admin shall be able to create, edit, activate, and deactivate user accounts.
- Inactive users shall not be allowed to log in.

### FR-02: Dashboard

- The system shall display an overview of inventory and business activities.
- The dashboard shall show total sales.
- The dashboard shall show total purchases.
- The dashboard shall show the current stock quantity.
- The dashboard shall display the number of low-stock products.

### FR-03: Product Management

- The system shall allow users to view and search products.
- The system shall allow authorized users to add and edit products.
- Each product shall have a unique SKU.
- Product information shall include:
  - Product name
  - SKU
  - Category
  - Description
  - Purchase price
  - Selling price
  - Current stock
  - Reorder level
  - Unit of measurement
  - Active status
- The Admin shall be able to deactivate products.
- Products with existing transaction history shall be deactivated rather than permanently deleted.

### FR-04: Category Management

- The system shall allow users to view product categories.
- Authorized users shall be able to add and edit categories.
- Each category shall have a unique name.
- Products shall be associated with their respective categories.

### FR-05: Purchase Management

- The system shall allow users to create and view purchase records.
- Each purchase shall be associated with a supplier.
- A purchase shall support multiple products.
- Each purchase item shall contain product, quantity, unit cost, and subtotal.
- The system shall calculate the purchase total automatically.
- Purchase records shall support the following statuses:
  - PENDING
  - RECEIVED
  - CANCELLED
- Stock shall increase only when a purchase is marked as RECEIVED.
- Receiving the same purchase more than once shall not increase stock repeatedly.

### FR-06: Sales Management

- The system shall allow users to create and view sales records.
- Each sale may be associated with a customer.
- A sale shall support multiple products.
- Each sale item shall contain product, quantity, unit price, and subtotal.
- The system shall calculate the sale total automatically.
- Sales shall support the following statuses:
  - DRAFT
  - COMPLETED
  - CANCELLED
- Stock shall decrease only when a sale is marked as COMPLETED.
- The system shall prevent users from selling quantities greater than the available stock.
- Completing the same sale more than once shall not decrease stock repeatedly.

### FR-07: Stock Management

- The system shall maintain the current stock quantity of each product.
- Stock shall automatically increase when purchases are received.
- Stock shall automatically decrease when sales are completed.
- The system shall support manual stock adjustments for damage, loss, and stock corrections.
- Every manual adjustment shall require a reason.
- The system shall maintain a stock movement history.
- Each stock movement shall record the product, quantity, movement type, source, user, and timestamp.

### FR-08: Customer Management

- The system shall allow users to view, add, and edit customer information.
- Customer information shall include name, phone number, email, address, and active status.
- The system