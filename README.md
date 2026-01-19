# Sahaaya-A-Hope-of-Beginning.
# SAHAAYA - Adoption Support Platform

A beginner-friendly React web application that connects loving families with children in need of adoption. The platform allows parents to view, add, edit, and manage child profiles similar to matrimony profile cards.

## Features

- **Home Page**: Displays the SAHAAYA mission statement
- **Children List**: View all child profiles in a card-based layout
- **Add Child**: Create new child profiles with image, name, age, description, and adoption status
- **Edit Child**: Update existing child profile details
- **CRUD Operations**: Full Create, Read, Update, Delete functionality
- **Status Management**: Toggle adoption status between "Available" and "Adopted"
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Dark Theme**: Modern black background interface

## Tech Stack

- **React 18**: Frontend framework
- **React Router DOM**: Navigation and routing
- **JSON Server**: Mock REST API backend
- **Vite**: Build tool and development server
- **CSS**: Custom styling with responsive design

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v16 or higher)
- npm (v7 or higher)

## Installation

1. Clone or download this repository
2. Navigate to the project directory:
   ```bash
   cd SAHAAYA
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

## Running the Application

You need to run two servers simultaneously:

### 1. Start JSON Server (Backend)

Open a terminal and run:
```bash
npm run server
```

This will start the JSON Server on `http://localhost:5000` and watch the `db.json` file for changes.

### 2. Start React Development Server

Open a **new terminal** and run:
```bash
npm run dev
```

This will start the Vite development server, typically on `http://localhost:5173`.

## Usage

1. Make sure both servers are running (JSON Server on port 5000 and React on port 5173)
2. Open your browser and navigate to the React app URL (usually `http://localhost:5173`)
3. Use the navigation menu to:
   - View the Home page with mission statement
   - Browse the Children List to see all profiles
   - Add new child profiles
   - Edit existing profiles
   - Update adoption status
   - Delete profiles

## API Endpoints

The application uses the following JSON Server endpoints:

- `GET http://localhost:5000/children` - Fetch all children
- `GET http://localhost:5000/children/:id` - Fetch a single child
- `POST http://localhost:5000/children` - Create a new child profile
- `PUT http://localhost:5000/children/:id` - Update a child profile
- `PATCH http://localhost:5000/children/:id` - Partially update a child profile (used for status updates)
- `DELETE http://localhost:5000/children/:id` - Delete a child profile

## Project Structure

```
SAHAAYA/
├── db.json                 # JSON Server database
├── index.html              # HTML entry point
├── package.json            # Dependencies and scripts
├── vite.config.js          # Vite configuration
├── README.md               # This file
└── src/
    ├── main.jsx            # React entry point
    ├── App.jsx             # Main app component with routing
    ├── index.css           # Global styles
    └── components/
        ├── Navigation.jsx  # Navigation bar
        ├── Home.jsx        # Home page component
        ├── ChildrenList.jsx # Children listing component
        ├── AddChild.jsx    # Add child form component
        └── EditChild.jsx   # Edit child form component
```

## Data Structure

Each child profile contains:
- `id`: Unique identifier (auto-generated)
- `name`: Child's name (string)
- `age`: Child's age (number)
- `description`: Detailed description (string)
- `image`: Image URL (string)
- `adoptionStatus`: Either "Available" or "Adopted" (string)

## Notes for Beginners

- **Components**: Each page is a separate React component in the `src/components` folder
- **Routing**: React Router handles navigation between pages
- **State Management**: Uses React hooks (`useState`, `useEffect`) for data management
- **API Calls**: Uses the Fetch API to communicate with JSON Server
- **Styling**: All styles are in `src/index.css` with a dark theme

## Troubleshooting

- **Port 5000 already in use**: Change the port in `package.json` script or stop the conflicting service
- **Port 5173 already in use**: Vite will automatically use the next available port
- **CORS errors**: Make sure JSON Server is running before starting the React app
- **Data not loading**: Verify JSON Server is running on port 5000 and `db.json` exists

## License

This project is created for educational purposes.

