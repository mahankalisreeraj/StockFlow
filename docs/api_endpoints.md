# API Endpoints List

1. **Authentication**

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| POST | /api/auth/login | Log in | Public |
| POST | /api/auth/logout | Log out | Authenticated |
| GET | /api/auth/me | Get logged-in user's details | Authenticated |

2. **Dashboard**

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| GET | /api/dashboard | Retrieve dashboard statistics | Both |

3. **Products and Categories**

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| GET | /api/products | View/search products | Both |
| GET | /api/products/:id | view individual product | Both |
| POST | /api/products | Add a product | Both |
| PUT | /api/products/:id | Update product details | Both |
| PATCH | /api/products/:id/deactivate | Deactivate a product | Admin |
| GET | /api/categories | View categories | Both |
| PUT | /api/categories/:id | Update a category | Both |
| POST | /api/categories | Add a category | Both |

4. **Customers and Suppliers**

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| GET | /api/customers | View customers | Both |
| POST | /api/customers | Add a customer | Both | 
| PUT | /api/customers/:id | Update a customer | Both |
| PATCH | /api/customers/:id/deactivate | Deactivate a customer | Admin |
| GET | /api/suppliers | View suppliers | Both |
| POST | /api/suppliers | Add a supplier | Both |
| PUT | /api/suppliers/:id | Update supplier details | Both | 
| PATCH | /api/suppliers/:id/deactivate | Deactivate a supplier | Admin |

5. **Purchases**

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| GET | /api/purchases | view purchases | Both |
| GET | /api/purchases/:id | View purchase details | Both | 
| POST | /api/purchases | Creating a purchase | Both |
| PATCH | /api/purchases/:id/recieve | Mark purchase as recived and increase stock | Both |
| PATCH | /api/purchases/:id/cancel | cancel a pending Purchase | Both |

6. **sales**

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| GET | /api/sales | View sales records | Both | 
| GET | /api/sales/:id | view sale details | Both |
| POST | /api/sales | Create a sale | Both |
| PATCH | /api/sales/:id/complete | Complete a sale and decrease stock | Both |
| PATCH | /api/sales/:id/cancel | cancel a pending/draft sale | Both |

7. **Stock Management**

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| GET | /api/stock | view current stock | Both |
| GET | /api/stock/movements | view stock movement history | Both | 
| POST | /api/stock/adjustments | Make a manual stock adjustment with a reason | Both | 

8. **User Management and Settings**

| Method | Endpoint | Purpose | Access |
|---|---|---|---|
| GET | /api/users | view users | Admin |
| POST | /api/users | Create a user | Admin |
| PUT | /api/users/:id | Update user details/role | Admin | 
| PATCH | /api/users/:id/deactivate | Deactivate a user | Admin |
| GET | /api/settings | view business settings | Admin | 
| PUT | /api/settings | Update business settings | Admin |