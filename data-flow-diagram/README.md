Data Flow Diagram (DFD) — Airbnb Clone Backend
 Objective

The purpose of this Data Flow Diagram (DFD) is to visualize how data moves through the Airbnb Clone Backend System, from inputs (user actions) to outputs (system responses).
It shows the flow of information between users, backend processes, the database, and external services such as payment gateways and email systems.

 DFD Level 0 — Context Diagram (Overview)

This level represents the entire system as a single process and identifies the main external entities that interact with it.

External Entities:

Guest → interacts with the system to search, book, and pay for properties.

Host → manages property listings and handles booking requests.

Admin → oversees system operations, manages users and listings.

Payment Gateway (e.g., Stripe/PayPal) → processes financial transactions.

Email/Notification Service → sends confirmation and update notifications.

Main Process:
Airbnb Clone Backend System

Data Stores:

User Data

Property Listings

Bookings

Payments

Reviews

Data Flows:

Guests send login credentials, booking details, and payment info.

Hosts send property data and updates.

System responds with booking confirmations, listings, and notifications.

Payment gateway sends transaction statuses.

 DFD Level 1 — Core Processes

This level breaks down the main system into key backend processes.

 Process 1: User Management

Input: Registration info, login credentials
Output: JWT token, user profile data
Data Store: User Data
External Entity: Guest / Host / Admin

Flow:
Users register or log in → system validates credentials → stores user record → returns authentication token.

 Process 2: Property Management

Input: Property details (title, description, location, price, photos)
Output: Confirmation of property creation or update
Data Store: Property Listings
External Entity: Host

Flow:
Host adds/updates listing → data stored in the database → system returns confirmation.

 Process 3: Booking Management

Input: Property ID, user ID, booking dates
Output: Booking confirmation or error message
Data Store: Bookings
External Entities: Guest, Host

Flow:
Guest requests booking → system checks availability → stores booking record → notifies host and guest.

 Process 4: Payment Processing

Input: Payment details, booking ID
Output: Payment confirmation or failure
External Entity: Payment Gateway
Data Store: Payments

Flow:
Guest initiates payment → backend sends data to payment gateway → gateway confirms → system stores transaction → sends confirmation email.

 Process 5: Reviews and Ratings

Input: Review text, rating score, booking ID
Output: Review confirmation
Data Store: Reviews
External Entities: Guest, Host

Flow:
Guest submits review → system validates and stores → review becomes visible for property.

 Process 6: Notifications

Input: Booking or payment event
Output: Email or in-app notification
External Entity: Notification Service

Flow:
System triggers event (e.g., booking confirmed) → sends message to email/notification service → notifies users.
