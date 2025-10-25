 Flowchart for System Process — User Registration Flow
 Objective

This flowchart illustrates the User Registration process in the Airbnb Clone backend system.
It represents how data moves and decisions are made from the moment a user submits their registration form until the system confirms successful account creation.

Description of the Process

The User Registration feature allows guests and hosts to create an account in the Airbnb system.
The process ensures data validation, duplication checks, password encryption, and secure storage in the database.

Flow Steps

Start Process
The process begins when a user opens the registration page and fills in the required details (name, email, password, role, etc.).

Input User Data
The user submits the registration form through the frontend.

Validate Input Fields
The backend validates the provided information:

Required fields (name, email, password) must not be empty.

Email must follow the correct format.

Password must meet security standards (e.g., minimum 8 characters, mix of letters and numbers).

Check if Email Already Exists
The system queries the database to verify whether the provided email is already registered.

If it exists → return an error message: “Email already in use.”

If it doesn’t exist → continue.

Encrypt Password
The password is hashed using bcrypt before being stored in the database to ensure security.

Save User to Database
The validated and processed user data is stored in the Users table.

Generate Authentication Token (JWT)
A unique JWT token is generated for the user to establish a session.

Send Confirmation Email (optional)
The system sends a welcome email to the user using an email service (e.g., SendGrid).

Return Success Response
The backend returns a success message and token to the frontend:
{"message": "User registered successfully", "token": "<jwt_token>"}

End Process
