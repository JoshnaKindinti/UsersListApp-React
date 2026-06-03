User Management App
A dynamic React application that allows users to view a list of team members, filter them in real-time using a search bar, and remove users from the list instantly.

## Project Overview
This project demonstrates core React concepts, including Class Components, Functional Components, State Management, Props passing, and Event Handling.

Key Features
Dynamic Search: Filters the user list in real-time as the user types into the search input field.

Delete Functionality: Allows users to remove a specific user profile from the list by clicking a delete (cross) button.

Stateful List: Tracks changes locally in the component state, ensuring UI updates instantly when a user is deleted or searched.

## Project Structure
The project follows a standard React directory layout. Below is the file structure indicating where each component and style sheet resides:

Plaintext
user-management-app/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   └── UserProfile/
│   │       ├── index.js          # UserProfile Functional Component
│   │       └── index.css         # Styles specific to UserProfile
│   ├── App.js                    # Main App Class Component (State & Logic)
│   ├── App.css                   # App-wide layouts and styles
│   ├── index.js                  # App entry point
│   └── index.css                 # Global reset and base styles
├── package.json                  # Dependencies and scripts
└── README.md                     # Documentation
Note: For the best organizational practices in React, the UserProfile code you provided should be placed in src/components/UserProfile/index.js, and its matching styles in index.css within that same folder.

## Component Breakdown
1. App.js (Class Component)
State: Manages searchInput (string) and userDetailsList (array of user objects).

Methods: * onChangeSearchInput: Updates the state with the current text in the search bar.

deleteUser: Expects a uniqueNo, filters it out of the current state array, and updates the view.

Logic: Dynamically filters the list of users before rendering them based on the search query.

2. UserProfile (Functional Component)
Props: Receives userDetails (object) and the deleteUser callback function.

Methods: * onDelete: Triggers when the delete button is clicked, passing the user's uniqueNo back up to the parent (App.js).

## Commands to Run the Project
Follow these steps to set up and run the application locally on your machine.

1. Clone the Repository
Bash
git clone <your-repository-url>
cd user-management-app
2. Install Dependencies
Ensure you have Node.js installed, then run the following command to download the required node_modules:

Bash
npm install
3. Start the Development Server
Runs the app in development mode.

Bash
npm start
