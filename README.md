# bank-appointment

## Activity 1: Project Planning for a Bank Appointment Management System

### Project Definition

The application will enable bank customers to book appointments for various services such as account opening, credit applications, financial advice, and more, thereby avoiding unnecessary waiting times and enhancing customer service.

### Specific Requirements

- **User Authentication**: Each user must register and authenticate to book an appointment. This ensures that only bank clients can use the service.
- **Types of Services**: Users should be able to choose the type of service they wish to avail themselves of at the bank to book the corresponding appointment.
- **Operating Hours**: Appointments should be bookable within the bank's operating hours, taking into account both business and non-business days.
- **Appointment Cancellation**: Users can cancel their appointments up to 24 hours before the scheduled time.
- **Notifications**: Users will receive booking confirmations and reminders for their appointments via email.

### Extra-Credits

- **Email Confirmation**: Implement a system that automatically sends booking and cancellation confirmations, as well as pre-appointment reminders.
- **User Profile**: Allow users to upload a profile picture to their account, enhancing personalization of the service.

## Activity 2: Execution

### 1. Writing User Stories

- **Story 1**: As a bank client, I want to register and log in to the app so I can book, modify, or cancel appointments.
- **Story 2**: As a client, I want to select the type of banking service I need to ensure I'm assigned the correct appointment.
- **Story 3**: As a client, I want to receive booking confirmations and reminders via email to keep track of my scheduled appointments.
- **Story 4**: As a client, I wish to cancel my appointment at least 24 hours in advance to rearrange my schedule without issues.

### 2. Database Schema

- **Users**: Contains information about the clients using the app.
  - Attributes: `id`, `firstName`, `lastName`, `email`, `password`, `profilePicture` (optional).
- **Appointments**: Records the appointments booked by users.
  - Attributes: `id`, `dateTime`, `typeOfService`, `userId`, `status` (booked, cancelled).
- **ServiceTypes**: Lists the types of services available at the bank.
  - Attributes: `id`, `description`.

These steps cover the initial planning and basic schemas to start developing the bank appointment management application. The next phase would involve developing the backend and frontend of the application, implementing the functionalities described in the user stories and following the database model.

## TypeScript Environment Setup

### Prerequisites

- [Node.js](https://nodejs.org/): Necessary for using `npm`.
- TypeScript: If you haven't installed TypeScript yet, you can add it globally to your system with `npm install -g typescript`.

### 1. Create the Project

```
mkdir backend && cd backend
npm init -y
```

### 2. Configure TypeScript

```
tsc --init
```

Configure `tsconfig.json` (optional):

```
{
    "compilerOptions": {
        "target": "ES5",
        "module": "commonjs",
        "rootDir": "./src",
        "outDir": "./dist",
        "strict": true
    },
    "include": ["src/**/*.ts"],
    "exclude": ["node_modules"]
}
```

### 3. (Optional) ESLint for TypeScript

```
npm install eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin --save-dev
```

Configure `.eslintrc`:

```
echo '{
"parser": "@typescript-eslint/parser",
"plugins": ["@typescript-eslint"],
"extends": [
    "eslint:recommended",
    "plugin:@typescript-eslint/recommended"
]
}' > .eslintrc.json
```

### 4. Write Code

Create a file `src/index.ts` and start writing your TypeScript code.

```
// src/index.ts
console.log("Hello, TypeScript!");
```

### 5. Compile and Run

```
tsc
node dist/index.js
```

## 6. Scripts in package.json

Add to facilitate tasks:

```
"scripts": {
    "build": "tsc",
    "start": "node ./dist/index.js",
    "dev": "tsc && node ./dist/index.js",
    "lint": "eslint . --ext .ts"
},
```
