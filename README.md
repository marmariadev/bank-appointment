# bank-appointment

# Activity 1: Planning the Bank Appointment Management Project

## Project Definition

The application will allow bank customers to book appointments for various services such as account opening, credit applications, financial advice, and more, eliminating unnecessary waiting times and optimizing customer service.

## Specific Requirements

- **User Authentication**: Every user must register and authenticate to be able to book an appointment. This ensures that only bank customers can use the service.
- **Types of Services**: Users should be able to choose the type of service they wish to receive at the bank to book the corresponding appointment.
- **Business Hours**: Appointments can only be booked during the bank's business hours, also taking into account business and non-business days.
- **Appointment Cancellation**: Users can cancel their appointments up to 24 hours before the scheduled time.
- **Notifications**: Users will receive confirmation and reminders of their appointments via email.

## Extra-Credits

- **Email Confirmation**: Implement a system that automatically sends booking and cancellation confirmations, as well as reminders before the appointment.
- **User Profile**: Allow users to upload a profile picture to their account, enhancing the personalization of the service.

# Activity 2: Execution

## 1. Writing User Stories

- **Story 1**: As a bank customer, I want to register and log in to the app, so I can book, modify, or cancel appointments.
- **Story 2**: As a customer, I want to select the type of banking service I need, to ensure I am assigned the correct appointment.
- **Story 3**: As a customer, I want to receive confirmations and reminders of my appointments via email, to keep control over my scheduled visits.
- **Story 4**: As a customer, I wish to cancel my appointment at least 24 hours in advance, to rearrange my schedule without issues.

## 2. Database Schema

- **Users**: Contains information about the clients using the app.
  - Attributes: `id`, `firstName`, `lastName`, `email`, `password`, `profilePicture` (optional).
- **Appointments**: Records the appointments booked by users.
  - Attributes: `id`, `dateTime`, `typeOfService`, `userId`, `status` (booked, cancelled).
- **ServiceTypes**: Lists the types of services available at the bank.
  - Attributes: `id`, `description`.

These steps cover the initial planning and basic schemas to start developing the bank appointment management application. The next phase would involve developing the backend and frontend of the application, implementing the functionalities described in the user stories, and following the established database model.
