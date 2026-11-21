# STOCKFLOW PROJECT

The purpose of this project is to develop a fully functional Inventory Management System that helps small businesses manage their inventory efficiently. It allows businesses to manage products, purchases, sales, stock levels, customers, and suppliers through a centralized system.

## Three-Layer Architecture:-

The three-layer architecture separates an application into three major components: the frontend, backend, and database. Each layer has its own responsibilities, making the application easier to develop, maintain, and scale.
- **Frontend** :  Responsible for client-side interactions and the user interface. It displays information, collects user input, and handles user interactions. It can also perform basic client-side validation.
- **Backend** : Acts as the communication and processing layer between the frontend and database. It receives requests, validates input, handles authentication and authorization, applies business logic, and communicates with the database.
- **Database** : Responsible for storing and retrieving application data. StockFlow uses PostgreSQL to store information about users, products, purchases, sales, customers, suppliers, and stock movements.

## Tech Stack 

This is the tech stack for my stockFlow project

1. **Frontend**: React, CSS/Tailwind CSS
2. **Backend**: Node.js & Express.js
3. **Database**: Postgre SQL

Supporting Tools:-
- **Version control** : git + github
- **API testing** : postman
- **UI Framework** : Figma

## Data flow between layers

1. The user interacts with the frontend, such as submitting a new product form.
2. The frontend sends an HTTP request to the appropriate REST API endpoint. The request may contain data in JSON format.
3. The backend receives the request and performs authentication, validation, and business logic checks.
4. If database operations are required, the backend executes the appropriate SQL queries against PostgreSQL.
5. The database performs the requested operation and returns the results to the backend.
6. The backend processes the results and sends an HTTP response, usually containing JSON data, back to the frontend.
7. The frontend displays the response to the user.
