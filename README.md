# Dosa Restaurant Management API


A RESTful backend API for managing operations at a Dosa restaurant, built using FastAPI and SQLite. This project provides full CRUD functionality for managing customers, menu items, and orders, and supports loading real-world order data from a JSON file.

## Project Structure

The project includes the following files:

- db.sqlite
- customers.json
- items.json
- init_db.py
- main.py
- load_from_json.py
- example_orders.json
- README.md
  

## API Overview

--> Customers
- POST /customers/ – Add a new customer
- GET /customers/{id} – Retrieve a customer by ID
- PUT /customers/{id} – Update customer details
- DELETE /customers/{id} – Remove a customer

--> Items
- POST /items/ – Add a menu item
- GET /items/{id} – Retrieve item details
- PUT /items/{id} – Update item info
- DELETE /items/{id} – Delete an item

--> Orders
- POST /orders/ – Create an order (linking customer and item)
- GET /orders/{id} – Get order details
- PUT /orders/{id} – Modify an order
- DELETE /orders/{id} – Cancel an order

## Features

- FastAPI framework with built-in interactive documentation
- SQLite database with relational integrity
- JSON-based data loading for quick setup
- Clean and modular Python code for easy maintenance
  
## Getting Started

1. Install Dependencies

- Ensure you have Python 3.7+ installed. Then install the required libraries.
- Run this on terminal: pip install fastapi uvicorn

2. Initialize the Database

- Run the following command to set up the database and create tables.
- Run this on terminal: python init_db.py

3. Load Sample Data

- Populate the database with data from the JSON file.
- Run this on terminal: python load_from_json.py

4. Launch the API Server

- Start the FastAPI server:
- Run on terminal: uvicorn main:app --reload
- Then open your browser and visit - http://127.0.0.1:8000/docs
- This will open the interactive Swagger UI for testing your API.
