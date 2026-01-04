# Stock-Management-API-Workflow-n8n-
This workflow is a complete REST API built in n8n to manage a car dealership stock for a web application.  It uses Google Sheets as the backend database for simplicity in this proof-of-concept version. The workflow supports standard CRUD operations for inventory management and allows the web app to interact with the stock seamlessly.

# Note: This is a demo version:
	•	allowed origins=*
	•	No authentication (API key)
A full production-ready version with authentication using API key and Base64 encoding will be provided in a future project.

# API Methods

1. GET /cars
	•	Retrieves all cars currently in inventory.
	•	Returns a JSON array with all car information stored in the Google Sheet.

2. POST /cars
	•	Adds a new car to the stock.
	•	Request body should include all relevant car details (model, year, price, etc.).
	•	Updates the Google Sheet with the new entry.

3. PATCH /cars/sold
	•	Moves cars from stock to sold.
	•	Updates the status of the selected car(s) in the Google Sheet.

4. PATCH /cars/restock
	•	Moves cars from sold back to stock.
	•	Updates the status of the selected car(s) accordingly.

5. PATCH /cars/update
	•	Updates information for a specific car in inventory.
	•	Can update fields like price, model, mileage, etc.

6. DELETE /cars
	•	Deletes one or more cars from the inventory.
	•	Removes entries from the Google Sheet.

⸻

# How It Works
	1.	Web app sends REST API requests to n8n.
	2.	n8n workflow reads or updates the Google Sheet depending on the method.
	3.	Returns structured JSON responses for web app consumption.

⸻

# Important Notes
	•	This workflow is a proof-of-concept for demonstration purposes.
	•	CORS is set to * (any origin allowed) — not suitable for production.
	•	No authentication or API key required in this version.
	•	Future project will include full API security and authentication with n8n and Base64.

⸻

# Use Cases
	•	Car dealership stock management
	•	Web app integration for inventory display and updates
	•	Proof-of-concept for n8n-based REST APIs
	•	Learning resource for CRUD operations via n8n + Google Sheets
