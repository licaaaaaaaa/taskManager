# Task Manager Frontend

A modern, responsive Next.js frontend for the Task Manager API.

## Features

- ✅ Beautiful, modern UI with Tailwind CSS
- ✅ Real-time task management
- ✅ Search and filter functionality
- ✅ Status updates with visual indicators
- ✅ Smooth animations with Framer Motion
- ✅ Responsive design for all devices
- ✅ JavaScript for simplicity

## Setup

1. **Install dependencies**
   ```bash
   npm install
   ```

2. **Environment Configuration**
   Create a `.env.local` file in the frontend directory:
   ```env
   NEXT_PUBLIC_API_URL=http://localhost:5000/api/v1
   ```

3. **Run the development server**
   ```bash
   npm run dev
   ```

   The frontend will be available at `http://localhost:3000`

## Technologies Used

- Next.js 14
- React 18
- JavaScript
- Tailwind CSS
- Framer Motion
- Lucide React (Icons)
- Axios

## Project Structure

```
frontend/
├── src/
│   ├── app/
│   │   ├── globals.css
│   │   ├── layout.js
│   │   └── page.js
│   ├── components/
│   │   ├── TaskCard.js
│   │   ├── TaskForm.js
│   │   └── SearchAndFilter.js
│   └── services/
│       └── api.js
├── package.json
├── tailwind.config.js
└── README.md
```

## API Integration

The frontend communicates with the backend API through the `api.ts` service file. Make sure the backend server is running on the correct port before starting the frontend.

## Development

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint
