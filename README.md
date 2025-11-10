
# StudySphere - Educational Ecosystem Platform

StudySphere is a comprehensive educational platform developed for WBAN Solution that revolutionizes student engagement through interactive learning experiences. Serving 150+ students and 10+ teachers, the platform combines gamification, AI-driven personalized feedback, and comprehensive class management to improve student grades by 55% while increasing platform engagement by 41%.

## Features

- **Comprehensive Class Management**: Complete educator toolkit for class creation, student enrollment, and progress monitoring with intuitive dashboard interfaces.
- **Interactive Learning Experience**: Engaging avatars, gamification elements, and point-based reward systems that motivate consistent student participation.
- **Real-Time Assessment System**: Instant quiz scoring, automated exam reminders, and immediate performance feedback for continuous learning improvement.
- **Meeting Scheduling & Management**: Integrated scheduling system for teacher-student interactions and class coordination.

## Tech Stack

### Frontend
- **React** – Dynamic and responsive user interface with component-based architecture
- **JavaScript/TypeScript** – Modern frontend development with type safety

### Backend
- **Node.js & Express.js** – Scalable server-side architecture with RESTful API design
- **Prisma ORM** – Type-safe database access and schema management
- **JWT Authentication** – Secure user authentication and session management

### Database
- **PostgreSQL** – High-availability relational database for secure data storage and complex queries

### Game Development
- **Unity & C#** – Cross-platform game engine for "Astro Blast" stress-management game

### Deployment & Infrastructure
- **Vercel** – Scalable cloud platform for frontend deployment and hosting

## Installation

### Prerequisites

- **Node.js 16+** - Required for backend services and React frontend
- **PostgreSQL 13+** - Database server for data persistence
- **Unity 2021.3 LTS+** - For game development (optional for core platform)

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-org/studysphere.git
   cd studysphere
   ```

2. **Set up environment variables**
   ```bash
   # Copy environment template
   cp .env.example .env
   
   # Configure your environment variables:
   # DATABASE_URL, JWT_SECRET, GEMINI_API_KEY, etc.
   ```

3. **Install dependencies**
   ```bash
   # Install backend dependencies
   cd server
   npm install
   
   # Install frontend dependencies
   cd ../client
   npm install
   ```

4. **Database setup**
   ```bash
   # Run Prisma migrations
   cd server
   npx prisma migrate dev
   npx prisma generate
   ```

5. **Start the development servers**
   ```bash
   # Start backend server (runs on port 3001)
   cd server
   npm run dev
   
   # Start frontend development server (runs on port 3000)
   cd ../client
   npm start
   ```

6. **Access the platform**
   - Frontend: `http://localhost:3000`
   - Backend API: `http://localhost:3001`
   - API Documentation: `http://localhost:3001/api-docs`

### Configuration Options

The platform can be customized through environment variables:

- **Database Configuration**: PostgreSQL connection settings
- **Authentication**: JWT secret keys and expiration times
- **AI Integration**: Gemini API keys and model parameters
- **File Upload**: Storage configuration for assignments and media
- **Email Services**: SMTP settings for automated notifications

### File Structure

```
studysphere/
├── client/                 # React frontend application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/         # Application pages and routes
│   │   ├── hooks/         # Custom React hooks
│   │   ├── services/      # API service layer
│   │   └── utils/         # Utility functions
│   └── public/            # Static assets and index.html
├── server/                # Node.js backend application
│   ├── src/
│   │   ├── controllers/   # Request handlers and business logic
│   │   ├── middleware/    # Authentication and validation middleware
│   │   ├── models/        # Prisma schema and database models
│   │   ├── routes/        # API route definitions
│   │   └── services/      # External service integrations
│   └── prisma/           # Database schema and migrations
├── game/                 # Unity Astro Blast game
│   ├── Assets/           # Game assets and scripts
│   ├── Scenes/           # Unity scenes
│   └── Scripts/          # C# game logic
└── docs/                 # Project documentation
```

### Running Different Components

#### 1. Full Development Environment
```bash
# Run all services with Docker Compose
docker-compose up -d

# Or run individually:
npm run dev:all
```

#### 2. Frontend Only (with API mocking)
```bash
cd client
npm run dev:mock
```

#### 3. Backend API Only
```bash
cd server
npm run dev
```

