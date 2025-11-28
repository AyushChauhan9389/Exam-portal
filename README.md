# Exam Portal

A modern, secure exam management system built with React, TypeScript, and Vite. This application provides a comprehensive platform for conducting online examinations with support for Safe Exam Browser (SEB) integration.

## Features

### Student Features
- 🔐 Secure authentication system
- 📊 Dashboard for viewing available exams
- ✍️ Real-time exam interface with timer
- 🖼️ Support for questions with images
- 🔒 Safe Exam Browser (SEB) enforcement for exam integrity
- 📱 Responsive design for various screen sizes

### Admin Features
- 👤 Separate admin authentication
- 📈 Comprehensive admin dashboard
- ✏️ Create and manage exams
- 📝 Add questions with multiple-choice options
- 🖼️ Image support for questions
- 👥 User management (individual and bulk creation)
- 📊 View and analyze exam results
- 🎯 Detailed student performance reports

## Tech Stack

- **Frontend Framework:** React 19
- **Language:** TypeScript
- **Build Tool:** Vite
- **Styling:** Tailwind CSS v4
- **Routing:** React Router v7
- **State Management:** Zustand
- **Data Fetching:** TanStack Query (React Query)
- **HTTP Client:** Axios
- **Icons:** Lucide React

## Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- Safe Exam Browser (for students taking exams)

## Getting Started

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd Exam-portal
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

## Available Scripts

- `npm run dev` - Start development server with hot reload
- `npm run build` - Build for production
- `npm run lint` - Run ESLint for code quality checks
- `npm run preview` - Preview production build locally

## Project Structure

```
src/
├── components/
│   ├── auth/
│   │   ├── ProtectedRoute.tsx       # Student route protection
│   │   └── ProtectedAdminRoute.tsx  # Admin route protection
│   ├── layouts/
│   │   └── PublicLayout.tsx         # Public pages layout
│   └── ui/
│       ├── Button.tsx               # Reusable button component
│       └── ImageZoom.tsx            # Image zoom functionality
├── hooks/
│   ├── useAuth.ts                   # Student authentication hook
│   └── useAdminAuth.ts              # Admin authentication hook
├── pages/
│   ├── Login.tsx                    # Student login page
│   ├── Dashboard.tsx                # Student dashboard
│   ├── ExamPage.tsx                 # Exam interface
│   └── admin/
│       ├── Login.tsx                # Admin login
│       ├── Dashboard.tsx            # Admin dashboard
│       ├── CreateExam.tsx           # Exam creation interface
│       ├── ExamDetails.tsx          # View/edit exam details
│       ├── ExamResults.tsx          # View exam results
│       ├── StudentExamResult.tsx    # Individual student results
│       ├── UserList.tsx             # User management
│       └── BulkCreateUsers.tsx      # Bulk user creation
├── services/
│   ├── api.ts                       # API client configuration
│   ├── auth.service.ts              # Authentication services
│   ├── exam.service.ts              # Exam-related services
│   └── admin.service.ts             # Admin services
├── store/
│   └── auth.store.ts                # Zustand auth store
├── types/
│   ├── auth.ts                      # Authentication types
│   ├── exam.ts                      # Exam-related types
│   └── admin.ts                     # Admin types
├── App.tsx                          # Main app component
└── main.tsx                         # Entry point
```

## Safe Exam Browser Integration

This application enforces Safe Exam Browser (SEB) for student exam sessions to ensure exam integrity and prevent cheating.

### For Students:

1. Download and install Safe Exam Browser from [https://safeexambrowser.org/](https://safeexambrowser.org/)
2. Launch the exam through the SEB link provided by your administrator
3. The application will only allow exam access when opened through SEB

### For Administrators:

- Admin panel is accessible through regular browsers
- No SEB requirement for administrative tasks
- Configure SEB settings as needed for your institution

## Routes

### Student Routes (Require SEB)
- `/login` - Student login
- `/dashboard` - Available exams
- `/exam/:examId` - Take exam

### Admin Routes (No SEB Required)
- `/admin/login` - Admin login
- `/admin/dashboard` - Admin overview
- `/admin/exams/create` - Create new exam
- `/admin/exams/:examId` - Exam details
- `/admin/exams/:examId/results` - Exam results
- `/admin/exams/:examId/results/:userId` - Student result details
- `/admin/users` - User list
- `/admin/users/bulk` - Bulk user creation

## Building for Production

```bash
npm run build
```

The build artifacts will be stored in the `dist/` directory.

## Development Guidelines

### Code Style
- Follow TypeScript best practices
- Use functional components with hooks
- Maintain proper type safety
- Follow ESLint rules

### Component Guidelines
- Keep components focused and single-purpose
- Use proper prop typing
- Implement error boundaries where appropriate
- Write reusable components in the `components/ui` directory

### State Management
- Use Zustand for global state (authentication, user data)
- Use TanStack Query for server state
- Use local state for component-specific data

## License

This project is private and proprietary.

## Support

For issues or questions, please contact the development team.
