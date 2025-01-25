# Expense_Tracker

## Overview
The Expense Tracker App is a full-stack application built using PostgreSQL, Express.js, React, and Node.js. This application allows users to manage their expenses efficiently, providing features for user authentication, expense management, and data visualization.

## Project Structure

### Backend
- **Models:**
  - **User .js:** Defines the user schema with fields for username and password. It includes pre-save middleware to hash passwords using bcrypt.
  - **Expense.js:** Defines the expense schema with fields for user, category, amount, comments, and timestamps.

- **Routes:**
  - **authRoutes.js:** Handles user authentication (signup and login).
  - **expenseRoutes.js:** Manages expenses (add, view, edit, and delete) with JWT-based authentication.
  - **server.js:** Main entry point for the backend. Configures middleware, connects to MongoDB, and defines route paths.

### Frontend
- **Components:**
  - **Login.js and Signup.js:** Handle user authentication.
  - **Dashboard.js:** Displays an overview of expenses and a form to add/edit expenses.
  - **ExpenseForm.js:** Allows users to input expense details.
  - **ExpenseTable.js:** Displays expenses in a sortable table.
  - **PieChart.js:** Visualizes expenses by category.
- **Styles:** CSS file (App.css) for styling.

## Key Features

### Authentication
- **Login/Signup:**
  - Users can create an account or log in to access their expenses.
  - The application uses JWT for secure authentication, storing the token in local storage for subsequent requests.

### Expense Management
- **Add/Edit/Delete Expenses:**
  - Users can add new expenses, edit existing ones, and delete expenses as needed.
  - The application communicates with the backend via API endpoints to manage expenses.

### Visualization
- **PieChart:**
  - Displays a category-wise distribution of expenses using a charting library (e.g., Chart.js or Recharts).

## How It Works Together
1. **User  Authentication:**
   - Users sign up or log in to generate a JWT.
   - The token is stored in local storage or cookies for subsequent requests.

2. **Expense Management:**
   - Authenticated users can add, edit, delete, or view expenses.
   - Data is fetched dynamically from the backend and displayed in the frontend.

3. **Visualization:**
   - Expenses are processed to generate insights (e.g., category distribution) and visualized using a chart.
     
## Technologies Used
- **Frontend:** React, Axios (for API communication), Chart.js or Recharts (for visualization)
- **Backend:** Node.js, Express.js, MongoDB, Mongoose, bcrypt (for password hashing), JSON Web Tokens (JWT)
