# Task Manager API + Next.js Frontend

A complete Task Manager application with Express.js REST API and Next.js frontend.

## Features

### Backend API
- ✅ CRUD operations for tasks
- ✅ Task status management (pending, in-progress, completed)
- ✅ Search tasks by keyword (title/description)
- ✅ Filter tasks by status
- ✅ RESTful API design
- ✅ MongoDB integration with Mongoose

### Frontend (Next.js)
- ✅ Modern, responsive UI
- ✅ Real-time task management
- ✅ Search and filter functionality
- ✅ Status updates with visual indicators
- ✅ Beautiful animations and transitions

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/v1/tasks` | Get all tasks (with search & filter) |
| GET | `/api/v1/tasks/:id` | Get task by ID |
| POST | `/api/v1/tasks` | Create new task |
| PATCH | `/api/v1/tasks/:id` | Update task |
| PATCH | `/api/v1/tasks/:id/status` | Update task status |
| DELETE | `/api/v1/tasks/:id` | Delete task |

### Query Parameters
- `search`: Search tasks by title or description
- `status`: Filter tasks by status (pending, in-progress, completed)

### Example API Usage
```bash
# Get all tasks
GET /api/v1/tasks

# Search tasks
GET /api/v1/tasks?search=meeting

# Filter by status
GET /api/v1/tasks?status=completed

# Search and filter
GET /api/v1/tasks?search=project&status=in-progress
```

## Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- npm or yarn

### Backend Setup

1. **Install dependencies**
   ```bash
   npm install
   ```

2. **Environment Configuration**
   Create a `.env` file in the root directory:
   ```env
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/taskmanager
   NODE_ENV=development
   ```

3. **Start MongoDB**
   Make sure MongoDB is running on your system or use MongoDB Atlas.

4. **Run the API server**
   ```bash
   # Development mode
   npm run dev
   
   # Production mode
   npm start
   ```

   The API will be available at `http://localhost:5000`

### Frontend Setup

1. **Navigate to frontend directory**
   ```bash
   cd frontend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   Create a `.env.local` file in the frontend directory:
   ```env
   NEXT_PUBLIC_API_URL=http://localhost:5000/api/v1
   ```

4. **Run the development server**
   ```bash
   npm run dev
   ```

   The frontend will be available at `http://localhost:3000`

## Project Structure

```
TaskManager/
├── src/
│   ├── config/
│   │   └── db.config.js
│   ├── controllers/
│   │   └── tasks.controller.js
│   ├── models/
│   │   └── tasks.model.js
│   ├── routes/
│   │   └── tasks.routes.js
│   ├── utils/
│   ├── app.js
│   └── server.js
├── frontend/          # Next.js application
├── package.json
└── README.md
```

## Task Model

```javascript
{
  title: String (required),
  description: String (required),
  status: String (enum: ['pending', 'in-progress', 'completed']),
  createdAt: Date,
  updatedAt: Date
}
```

## Technologies Used

### Backend
- Express.js
- MongoDB
- Mongoose
- CORS
- dotenv

### Frontend
- Next.js 14
- React
- JavaScript
- Tailwind CSS
- Framer Motion
- Axios

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

MIT License
