
# StudySphere - Educational Ecosystem Platform

StudySphere is a comprehensive educational platform developed for WBAN Solution that revolutionizes student engagement through interactive learning experiences. Serving 150+ students and 10+ teachers, the platform combines gamification, AI-driven personalized feedback, and comprehensive class management to improve student grades by 55% while increasing platform engagement by 41%.

## Features

- **Comprehensive Class Management**: Complete educator toolkit for class creation, student enrollment, and progress monitoring with intuitive dashboard interfaces.
- **Interactive Learning Experience**: Engaging avatars, gamification elements, and point-based reward systems that motivate consistent student participation.
- **AI-Powered Personalized Feedback**: Gemini LLM integration delivers adaptive feedback generation, identifying knowledge gaps and providing personalized learning insights.
- **Real-Time Assessment System**: Instant quiz scoring, automated exam reminders, and immediate performance feedback for continuous learning improvement.
- **Meeting Scheduling & Management**: Integrated scheduling system for teacher-student interactions and class coordination.
- **Facial Verification Security**: Python and dlib-powered facial recognition for secure exam authentication and academic integrity.
- **Stress Management Gaming**: Unity-developed "Astro Blast" game providing students with engaging stress-relief activities.

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

### AI & Machine Learning
- **Google Gemini LLM** – Advanced language model for adaptive feedback generation and personalized learning insights
- **Python & dlib** – Computer vision library for facial verification and biometric authentication

### Game Development
- **Unity & C#** – Cross-platform game engine for "Astro Blast" stress-management game

### Deployment & Infrastructure
- **Vercel** – Scalable cloud platform for frontend deployment and hosting

## Installation

### Prerequisites

- **Node.js 16+** - Required for backend services and React frontend
- **PostgreSQL 13+** - Database server for data persistence
- **Python 3.8+** - For facial verification services
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
├── facial-verification/   # Python facial recognition service
│   ├── main.py           # FastAPI server for face verification
│   ├── models/           # Pre-trained dlib models
│   └── utils/            # Image processing utilities
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

#### 4. Facial Verification Service
```bash
cd facial-verification
pip install -r requirements.txt
python main.py
```

### Platform Usage

Once the platform is running:

1. **Teacher Dashboard**: Access comprehensive class management, student enrollment, and progress analytics
2. **Student Portal**: Interactive learning interface with gamified elements and real-time feedback
3. **Assessment Center**: Create and manage quizzes with automated grading and instant results
4. **Meeting Scheduler**: Coordinate teacher-student meetings and virtual classroom sessions
5. **Analytics Dashboard**: Monitor student performance, engagement metrics, and learning outcomes
6. **Game Integration**: Access Astro Blast for stress management and student well-being

### Educational Impact

**For Students:**
- 55% improvement in grades through personalized AI feedback
- 41% increase in platform engagement time
- Reduced academic stress through gamification and interactive elements
- Enhanced learning retention with immediate feedback loops

**For Educators:**
- Streamlined class management and administrative tasks
- Real-time insights into student performance and engagement
- Automated assessment and grading capabilities
- Data-driven teaching strategy optimization

### Production Deployment

For production environments:

1. **Environment Setup**: Configure production environment variables and database connections
2. **Security Configuration**: Enable HTTPS, configure CORS policies, and secure API endpoints
3. **Performance Optimization**: Implement caching strategies and database optimization
4. **Monitoring & Logging**: Set up error tracking, performance monitoring, and audit logging
5. **Backup Strategy**: Configure automated database backups and disaster recovery

### API Documentation

The platform provides comprehensive RESTful APIs:

- **Authentication Endpoints**: User registration, login, and JWT token management
- **Class Management**: CRUD operations for classes, enrollments, and assignments
- **Assessment APIs**: Quiz creation, submission handling, and automated grading
- **Analytics Endpoints**: Student progress tracking and performance analytics
- **Notification Services**: Automated reminders and communication systems

### Troubleshooting

**Common Issues:**

- **Database Connection**: Verify PostgreSQL is running and connection string is correct
- **API Authentication**: Check JWT token validity and API key configurations
- **Facial Verification**: Ensure Python dependencies are installed and camera permissions are granted
- **Game Integration**: Verify Unity WebGL build is properly deployed

**Performance Optimization:**

- Enable database query optimization and indexing
- Implement Redis caching for frequently accessed data
- Configure CDN for static asset delivery
- Optimize React bundle size and implement code splitting

### Contributing

StudySphere is developed for WBAN Solution to enhance educational outcomes through technology innovation. The platform demonstrates significant impact in student engagement and academic performance while providing educators with powerful tools for modern classroom management.
