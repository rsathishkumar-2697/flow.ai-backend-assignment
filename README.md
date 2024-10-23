   Floww.ai Node JS - Backend Assignment: Personal Expense Tracker

Personal Expense Tracker Overview This project is a RESTful API for managing personal financial transactions. It allows users to record income and expenses, retrieve past transactions, and generate summary reports, providing a basic personal financial tracking system.

Table of Contents:

1.Features

2.Technologies

3.API Endpoints

4.Error Handling

5.Postman Documentation

6.GitHub Repository
   

1. Features:

   The API includes the following functionalities:

   Create new transactions (both income and expense).
   
   Read all or specific transactions.
   
   Update existing transactions.
   
   Delete transactions.
   
   Generate a summary of all transactions, showing total income, total expenses, and current balance.

2. Technologies:
   
   The project is built with the following stack:

   Node.js: JavaScript runtime environment.

   Express.js: Web framework for Node.js, used to create the API routes.

   SQLite: Lightweight database for storing transaction data.

   Postman: API testing tool used to test the endpoints.

3. API Endpoints:
   
   Here is a detailed list of all available API endpoints:

          Method	                 Endpoint	                                 Description

          POST	                     /transactions	                      Create a new transaction ![Screenshot_Create](https://github.com/user-attachments/assets/e41bc908-149a-4aa6-9b3b-a110d45e29a0)


          GET	                     /transactions	                      Retrieve all transactions ![Screenshot_Retrieve_data_preview](https://github.com/user-attachments/assets/a7d7ad0a-b004-45d8-a208-60b26b3a189b)


          GET	                     /transactions/:id	                      Retrieve a transaction by ID ![Screenshot_Retrieve_Data](https://github.com/user-attachments/assets/95ee787b-edd6-44df-b295-c24f52728983)


          PUT	                     /transactions/:id	                      Update a transaction by ID ![Screenshot_Update](https://github.com/user-attachments/assets/7b2fb143-5c50-4a5c-911c-eb3f7f8328fa)


          DELETE	               /transactions/:id	                     Delete a transaction by ID ![Screenshot_Delete](https://github.com/user-attachments/assets/50b58398-8efa-42c2-8748-8223a6a3db6b)


          GET	                     /summary	                             Retrieve a summary (total income/expense) ![Screenshot_Summary1](https://github.com/user-attachments/assets/c039a5b6-ad76-4a7e-8341-fa095da9f0a6)



Example Request & Response

POST /transactions

  json

  {

    "type": "expense",
	
    "category": "Food",
	
    "amount": 30,
	
    "date": "2024-10-23",
	
    "description": "Groceries"
	
  }

Response:

json

{

  "message": "Transaction added successfully",
	
  "transaction": {
	
    "id": 1,
		
    "type": "expense",
		
    "category": "Food",
		
    "amount": 30,
		
    "date": "2024-10-23",
		
    "description": "Groceries"
		
  }
	
}



4. Error Handling:

     All API endpoints include basic error handling. If an invalid request is made, the API will return an error with an appropriate status code and message.

Example:

404 Not Found: If a requested transaction does not exist.

400 Bad Request: If invalid data is provided in the request body.

Example Error Response

json

{

  "error": "Transaction not found"
	
}

5. Postman Documentation:
   
   To make testing easier, here are the steps to test your API using Postman:

   Set up API calls: Use the above-listed endpoints in Postman and send requests.
   
   Capture screenshots: Take screenshots of successful responses for each API call.

6.GitHub Repository:

   Source code push into GitHub Repository.

