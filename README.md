# Smart Time & Task Manager

A full-stack application for managing tasks and tracking time efficiently. This project is built using Node.js, Express, Sequelize ORM, and React with TypeScript.

## Features

- **User Authentication**: Secure registration, login, and profile management
- **Task Management**: Create, read, update, and delete tasks
- **Time Tracking**: Start and stop time tracking for tasks
- **Task Categorization**: Organize tasks with status and priority levels
- **Dashboard**: Visual overview of task statistics and recent activities
- **Reports & Analytics**: Detailed insights into time spent and productivity
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## Tech Stack

### Backend
- **Node.js**: JavaScript runtime
- **Express.js**: Web framework
- **Sequelize ORM**: Database ORM
- **PostgreSQL**: Database (configurable)
- **JWT Authentication**: Secure user authentication
- **Morgan**: HTTP request logger

### Frontend
- **React**: UI library
- **TypeScript**: Type-safe JavaScript
- **Tailwind CSS**: Utility-first CSS framework
- **React Router**: Client-side routing
- **Axios**: HTTP client
- **Chart.js**: Data visualization
- **Context API**: State management

## Project Structure

```
├── src/                  # Backend source code
│   ├── config/           # Configuration files
│   ├── controllers/      # Route controllers
│   ├── middleware/       # Custom middleware
│   ├── models/           # Database models
│   ├── routes/           # API routes
│   ├── utils/            # Utility functions
│   └── index.js          # Entry point
├── client/               # Frontend source code
│   ├── src/              # React application source
│   │   ├── assets/       # Static assets
│   │   ├── components/   # Reusable UI components
│   │   ├── context/      # React context providers
│   │   ├── pages/        # Page components
│   │   ├── services/     # API services
│   │   └── utils/        # Utility functions
│   ├── public/           # Public assets
│   └── index.html        # HTML entry point
├── .env                  # Environment variables
├── package.json          # Backend dependencies
└── README.md            # Project documentation
```

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- PostgreSQL (optional, can use mock database for development)

### Installation

1. Clone the repository

```bash
git clone https://github.com/yourusername/smart-time-task-manager.git
cd smart-time-task-manager
```

2. Install backend dependencies

```bash
npm install
```

3. Install frontend dependencies

```bash
cd client
npm install
```

4. Create a `.env` file in the root directory with the following variables:

```
NODE_ENV=development
PORT=5000
JWT_SECRET=your_jwt_secret
DB_HOST=localhost
DB_USER=postgres
DB_PASS=your_password
DB_NAME=task_manager
```

### Running the Application

1. Start the backend server

```bash
npm run dev
```

2. Start the frontend development server

```bash
cd client
npm run dev
```

3. Access the application at http://localhost:5173

## Development Mode

This project uses a mock database implementation for local development to avoid the need for setting up a local SQL Server or PostgreSQL. The mock database:

- Uses in-memory storage
- Provides mock implementations of Sequelize methods
- Automatically initializes with sample data
- Requires no additional setup

## API Documentation

The backend API provides the following endpoints:

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login a user and get JWT token
- `GET /api/auth/me` - Get current user profile (requires authentication)

### Tasks
- `GET /api/tasks` - Get all tasks for current user
- `GET /api/tasks/:id` - Get a specific task
- `POST /api/tasks` - Create a new task
- `PUT /api/tasks/:id` - Update a task
- `DELETE /api/tasks/:id` - Delete a task

### Time Tracking
- `POST /api/tasks/:id/start` - Start time tracking for a task
- `POST /api/tasks/:id/stop` - Stop time tracking for a task
- `GET /api/tasks/:id/time-entries` - Get time entries for a task
- `GET /api/tasks/stats` - Get task statistics

## Development Roadmap

- ✅ Backend API setup and database configuration
- ✅ Authentication and core task management APIs
- ✅ Frontend setup with React, TypeScript and Tailwind CSS
- ✅ Basic routing and application structure
- 🔄 Task management UI implementation
- 🔄 Time tracking functionality
- ⬜ Dashboard with statistics and reports
- ⬜ User settings and profile management
- ⬜ Testing and optimization
- ⬜ Production deployment

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- React team for the amazing UI library
- Tailwind CSS for the utility-first CSS framework
- Express.js team for the robust web framework
- Sequelize team for the powerful ORM