# Qr Ticketing System
Ticketing system for a museum 

## Introduction

This is a Ticketing system for a Musuem and heritage structure, in which front end (client side) is developed using React JS and back end (server side) is developed using Node JS and Express JS. This web application use MongoDB as the database, which is a cross-platform document-oriented database.

Users can register on the system. A verification email will be sent to the customer email. he needs to confirm it before login to the system. After registration, a customer can log in to the system using email and password otherwise he can use social login. Admin can also login to the system using the same login by inputting the email and password provided by the main admin.

Once the main admin creates an admin the created admin will receive a confirmation email and for customers also once they are registered, they will receive a verification email to activate their account.

Using their profile, they can view their booking history. Both registered users and unregistered users can view the cost of booking. but only logged in users can confirm the reservation. Once the reservation is confirmed user will receive an email that includes the reservation details and unique QR code for that reservation. The user can scan the QR code at the theatre . and get a ticket. When they are getting into the theatre, they need to scan the QR code.  

## Architectural Diagrams

This application follows Model-View-Controller (MVC) architecture. The view is implemented using ReactJS which is using a composite view pattern. The controller and model is implemented using Node.js, MongoDB NoSQL database is connected to the back end. Front end and the back end communicate through REST API calls.

<p></p><br />

<img src="https://i.ibb.co/ZL3rYsR/Capture27.png" alt="Capture27" border="0">
Figure 1: component diagram
<p></p><br />

## Features of the application



### 1)  Real-time ticket availability

In this application users can provide the reservation details and check the current availability of seats and make the booking. Our application tracks the reservations made before and displays the actual seats available at the time user going to make a reservation.
When make booking user needs to add start and the destination locations, theatre, class, time, ticket quantity and the date of booking. Once the data entered the application get the previous bookings for same  time and date and subtract by the number of seats available.

Even if the user doesn’t have an account created for the application, they can view the availability of seats. Once user needs to make the reservation, they need to have an account.
<p></p><br />


### 2) Email and SMS notification

Once user makes a reservation the application will generate a QR code to track the reservation. Then an email will be sent to the user’s email along with reservation details and generated QR code, which will be used to print the ticket at the railway ..
Also, the system will send a text message to the user’s registered mobile number with the reservation details.
<p></p><br />

### 3)  Discount for Government officers

This is a new feature we introduced to the application. If the user is a government employee, they can have special discounts. Once user gives their NIC when registering, that NIC is validated using government web service to ensure that user is eligible to have discounts. If the user is eligible for discounts, it will be added to the reservation.

### 4)  Pay by card and cash options

In the specification of this application does not have direct payment method. According to the specification users must top up their account and then pay the reservation fee. That includes additional user interaction and the user friendliness of the application will go down.

Therefore, we added direct payment method and pay by cash option. User can select any option when making a reservation. If user select card, then user need to add valid card details. Or users can select pay by cash and pay at the railway ..

### 5)  Computerize administration panel

#### i) User Management

As an improvement to the specification, In the user management section, there is a list of users, administrators can disable a particular user from that list. After disabling the user cannot access the account using their credentials. An error message will be displayed to the user. We’ve added this feature because if any customer misbehaves some way, there should be a way to disable that user from the system. In the specification, there wasn’t a way to disable a user.
  
As another improvement to the specification administrators can edit customer account. such as their email. In the user view, users can’t change their email addresses. however, if the special request comes from the client, administrators can update the specific customer’s email address and other details. 

