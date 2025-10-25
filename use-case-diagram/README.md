Airbnb Clone Backend — Use Case Diagram (Text Version)
 Actors

Guest (User)

Host

Admin

Payment Gateway (Stripe / PayPal)

Email Service (SendGrid / Mailgun)

 Guest Use Cases

Main Goal: Find, book, and pay for accommodations.

Register an account

Log in / Log out

View and update profile

Search for properties

Filter properties (by location, price, amenities, number of guests)

View property details

Make a booking

Cancel a booking

Make payment for a booking

View booking history

Leave a review and rating for a property

Receive notifications (booking confirmation, payment confirmation, cancellations)

 Host Use Cases

Main Goal: List and manage rental properties.

Register an account

Log in / Log out

Add new property listing (title, description, price, amenities, availability)

Edit property listing

Delete property listing

View all listed properties

Manage booking requests (approve or decline)

Respond to reviews

Receive notifications (new booking, cancellations, payments received)

 Admin Use Cases

Main Goal: Manage and monitor system operations.

Manage users (activate, suspend, or delete accounts)

Manage property listings

Manage bookings

Manage payments and refunds

Monitor reviews and user activity

Generate reports (users, listings, revenue, etc.)

Handle system errors or complaints

 Payment Gateway Use Cases (External System)

Main Goal: Handle secure transactions.

Process guest payments

Transfer payouts to hosts

Handle refunds or failed transactions

Confirm successful payments to the backend system

 Email Service Use Cases (External System)

Main Goal: Send automated communication.

Send registration confirmation emails

Send booking confirmation and cancellation emails

Send payment confirmation emails

Send notifications about reviews or updates

System Notes

Includes: Authentication, Validation, Error Handling

Extends:

“Make Payment” → extends “Create Booking”

“Leave Review” → extends “View Booking History”

“Send Notification” → extends “Booking Confirmation” and “Payment Confirmation”
