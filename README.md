
# E-commerce API Testing Project (Postman)

## Tech
- Postman (Collection, Environment, Tests)
- Public API: https://fakestoreapi.com

## How to Import
1. Open Postman → Import.
2. Import `Ecommerce_API_Testing.postman_collection.json`.
3. Import `Ecommerce_API_Environment.postman_environment.json`.
4. Select the environment in the top-right of Postman.

## How to Run
- Run requests one-by-one or use **Collection Runner**.
- Flow:
  1) **GET - All Products**
  2) **POST - Create Product** → saves `productId` to environment
  3) **GET - Product by ID (from POST)** → uses saved `productId`
  4) **PUT** → full update using `productId`
  5) **PATCH** → partial update using `productId`
  6) **DELETE** → delete using `productId`

## What is Tested
- Status codes, response times, JSON format
- Field checks and basic schema expectations
- Variable chaining (`productId` from POST used in later calls)

## Notes
- Fake Store API is public and sometimes returns mocked-data on writes.
- For real auth flows, plug in a private API and add auth headers.
