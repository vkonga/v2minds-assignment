Here's a README documentation for your project, which includes both the frontend React application and the backend Node.js server:


# Notes Application

This is a simple notes application built with a React frontend and a Node.js/Express backend. The application allows users to create, view, and delete notes.

## Features

- **Create Notes**: Users can create new notes by entering content and submitting it.
- **View Notes**: Users can view a list of all saved notes.
- **Delete Notes**: Users can delete notes from the list.

## Technologies Used

- **Frontend**: React, CSS
- **Backend**: Node.js, Express
- **Database**: SQLite
- **Other**: uuid (for unique ID generation), cors (for handling Cross-Origin Resource Sharing)

## Setup Instructions

### Prerequisites

- Node.js and npm (Node Package Manager) should be installed on your machine.
- SQLite should be installed for database management.

### Installation

1. **Clone the repository**:

   git clone https://github.com/vkonga/v2minds-assignment.git
   cd v2minds-assis
   

2. **Install dependencies**:

   - For the backend:
     cd v2minds-assignment
     npm install
     

   - For the frontend:
     cd v2minds-frontend
     npm install
     

## Running the Application

### Backend

1. **Initialize the database**:

   - Ensure you have an SQLite database named `notes.db` in the backend directory.

2. **Start the server**:

   cd v2minds-assignment
   nodemon index.js or node index.js
   

   The backend server will run on `http://localhost:3000`.

### Frontend

1. **Start the React app**:

   cd v2minds-frontend
   npm start
   

   The frontend will be available at `http://localhost:3000`.

## API Documentation

### Add a Note

- **Endpoint**: `POST /notes`
- **Description**: Adds a new note.
- **Request Body**: JSON object containing `id`, `content`, and `createdAt`.
- **Response**: Returns a JSON object with the added note details.

### Get All Notes

- **Endpoint**: `GET /notes`
- **Description**: Retrieves all notes.
- **Response**: Returns a JSON array of note objects.

### Delete a Note

- **Endpoint**: `DELETE /notes/:id`
- **Description**: Deletes a note by its ID.
- **Request Params**: `id` (The ID of the note to delete).
- **Response**: Returns a JSON message indicating success or failure.

## Frontend Details

The frontend is a React application that includes the following components and features:

- **Home Component**: The main component that handles note creation, viewing, and deletion.
- **State Management**: Uses React's `setState` for managing the state of notes, loading status, and error messages.
- **UI Elements**: Includes a form for adding notes, a button for fetching the notes list, and delete buttons for removing notes.

## Backend Details

The backend is built using Node.js and Express. It includes the following features:

- **SQLite Database**: Stores notes with `id`, `content`, and `created_at` fields.
- **Express Middleware**: Uses `express.json()` for parsing JSON request bodies and `cors()` for handling CORS.
