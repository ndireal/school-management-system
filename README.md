# School Management System

A modern, web-based school management system that streamlines school administration and academic processes.

## 🎯 Features

- **Student Management**: Enrollment, profile management, and records
- **Teacher & Staff Management**: Employee profiles and role assignment
- **Class & Subject Management**: Course scheduling and organization
- **Attendance Tracking**: Real-time attendance marking and reports
- **Timetable Generation**: Automated schedule creation
- **Assignment & Exam Management**: Assignment posting and exam scheduling
- **Grading System**: Grade entry, GPA calculation, report cards
- **Fee Management**: Payment tracking and fee collection
- **Parent Portal**: Access to student progress and notifications
- **Student Portal**: Assignment submission, grade viewing
- **Role-Based Access Control**: Admin, Teacher, Student, Parent roles
- **Notifications**: Real-time alerts and announcements

## 🏗️ Project Structure

```
school-management-system/
├── backend/              # Express.js/NestJS API server
├── frontend/             # React TypeScript application
├── shared/               # Shared types and utilities
├── docker-compose.yml    # Docker composition
├── .env.example          # Environment variables template
└── docs/                 # Documentation
```

## 🛠️ Technology Stack

### Frontend
- **React 18+** with TypeScript
- **Vite** for fast build tooling
- **TailwindCSS** for styling
- **Zustand** for state management
- **React Query** for API data fetching
- **React Router** for navigation
- **Axios** for HTTP client

### Backend
- **Node.js** with Express.js
- **TypeScript** for type safety
- **Prisma ORM** for database management
- **PostgreSQL** as primary database
- **JWT** with refresh tokens for authentication
- **Bcrypt** for password hashing
- **Multer** for file uploads
- **Cloudinary** for image storage
- **Joi** for data validation

### DevOps & Infrastructure
- **Docker** & **Docker Compose** for containerization
- **ESLint & Prettier** for code quality
- **Jest** for testing
- **GitHub Actions** for CI/CD

## 🚀 Quick Start

### Prerequisites
- Node.js >= 18
- PostgreSQL >= 12
- Docker & Docker Compose
- npm or yarn

### Development Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/ndireal/school-management-system.git
   cd school-management-system
   ```

2. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

3. **Using Docker Compose (Recommended)**
   ```bash
   docker-compose up -d
   ```

4. **Manual Setup**
   
   Backend:
   ```bash
   cd backend
   npm install
   npx prisma migrate dev
   npm run dev
   ```

   Frontend:
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

5. **Access the application**
   - Frontend: http://localhost:5173
   - Backend API: http://localhost:5000
   - API Documentation: http://localhost:5000/api/docs

## 📚 API Documentation

API documentation is available at `/api/docs` when the backend server is running.

## 📦 Database Schema

See `backend/prisma/schema.prisma` for the complete database schema.

## 🔐 Authentication

The system uses JWT-based authentication with the following flow:
- User login with email and password
- Access token (15 minutes) and Refresh token (7 days) returned
- Refresh token used to obtain new access tokens
- All protected routes require valid JWT in Authorization header

## 🎨 Project Structure Details

### Backend
```
backend/
├── src/
│   ├── config/          # Configuration files
│   ├── controllers/      # Route controllers
│   ├── services/         # Business logic
│   ├── models/           # Data models
│   ├── middlewares/      # Custom middlewares
│   ├── routes/           # API routes
│   ├── utils/            # Utility functions
│   ├── validators/       # Input validation
│   ├── types/            # TypeScript types
│   └── app.ts           # Express app setup
├── prisma/
│   ├── schema.prisma    # Database schema
│   └── migrations/      # Database migrations
├── tests/               # Test files
├── .env.example         # Environment template
└── package.json
```

### Frontend
```
frontend/
├── src/
│   ├── components/      # Reusable components
│   ├── pages/          # Page components
│   ├── hooks/          # Custom React hooks
│   ├── services/       # API service layer
│   ├── store/          # Zustand stores
│   ├── types/          # TypeScript types
│   ├── utils/          # Utility functions
│   ├── assets/         # Static assets
│   ├── styles/         # Global styles
│   ├── App.tsx         # Root component
│   └── main.tsx        # Entry point
├── public/             # Public assets
└── package.json
```

## 🔄 Development Workflow

1. Create a feature branch: `git checkout -b feature/your-feature`
2. Make your changes
3. Run tests: `npm test`
4. Commit changes: `git commit -am 'Add your message'`
5. Push to branch: `git push origin feature/your-feature`
6. Create a Pull Request

## 📝 Coding Standards

- Use TypeScript for type safety
- Follow ESLint and Prettier configurations
- Write meaningful commit messages
- Add tests for new features
- Document complex functions
- Use meaningful variable and function names

## 🧪 Testing

```bash
# Backend tests
cd backend && npm test

# Frontend tests
cd frontend && npm test
```

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Please follow the development workflow above.

## 📞 Support

For issues and questions, please create an issue on GitHub.
