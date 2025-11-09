# Job Portal Frontend

A modern, responsive React.js frontend application for the Job Portal platform. This application provides an intuitive user interface for job seekers, recruiters, and administrators to interact with the job portal system.

## Features

### User Interface

- **Modern UI/UX** - Clean, intuitive interface built with Tailwind CSS
- **Interactive Components** - Rich user interactions with React components
- **Real-time Updates** - Live data updates using React Query
- **Form Validation** - Client-side validation with React Hook Form

### User Roles & Capabilities

#### Job Seekers

- Browse and search job listings
- Filter jobs by category, location, and salary
- Apply for jobs with one click
- View application history and status
- Manage personal profile and resume

#### Recruiters

- Post new job listings
- Manage existing job postings
- View and manage job applications
- Access recruiter dashboard with analytics

#### Administrators

- User management interface
- Platform statistics and analytics
- Job posting oversight
- Administrative dashboard

## Tech Stack

- **React 18.2.0** - Modern React with hooks and functional components
- **React Router DOM 6.18.0** - Client-side routing and navigation
- **Tailwind CSS 3.3.5** - Utility-first CSS framework
- **Styled Components 6.1.1** - CSS-in-JS for component-level styling
- **Vite 4.4.5** - Fast build tool and development server
- **React Query (@tanstack/react-query) 5.8.4** - Server state management
- **React Hook Form 7.48.2** - Efficient form handling and validation
- **Axios 1.6.2** - HTTP client for API requests
- **React Icons 4.11.0** - Comprehensive icon library
- **Recharts 2.10.1** - Data visualization and charts
- **SweetAlert2 11.10.0** - Beautiful, responsive alerts
- **React Paginate 8.2.0** - Pagination component
- **Day.js 1.11.10** - Date manipulation library

## Project Structure

```
src/
├── assets/                    # Static assets
│   ├── css/
│   │   └── wrappers/         # Styled component wrappers
│   └── media/                # Images and media files
├── components/               # Reusable React components
│   ├── AllJobsPage/         # Job listing related components
│   │   ├── JobCard.jsx      # Individual job card component
│   │   ├── JobsListCom.jsx  # Job list container
│   │   ├── PaginationCom.jsx # Pagination component
│   │   └── SearchAndFilter.jsx # Search and filter functionality
│   ├── Home Page/           # Landing page components
│   │   ├── Brands.jsx       # Featured brands section
│   │   ├── HowWorks.jsx     # How it works section
│   │   ├── PopularCategory.jsx # Popular job categories
│   │   ├── Team.jsx         # Team section
│   │   └── Testimonial.jsx  # User testimonials
│   ├── MyJobsPage/          # Job management components
│   │   ├── Applicant.jsx    # Applicant view components
│   │   └── Recruiter.jsx    # Recruiter view components
│   └── shared/              # Shared components
│       ├── CommonProtectRoute.jsx # Route protection
│       ├── DashboardNavbar.jsx    # Dashboard navigation
│       ├── Loading.jsx            # Loading components
│       ├── Navbar.jsx            # Main navigation
│       └── [other shared components]
├── context/                 # React context providers
│   ├── JobContext.jsx      # Job-related state management
│   └── UserContext.jsx     # User-related state management
├── Layout/                  # Layout components
│   ├── DashboardLayout.jsx # Dashboard layout wrapper
│   └── HomeLayout.jsx      # Home page layout wrapper
├── pages/                   # Page components
│   ├── AddJob.jsx          # Add new job page
│   ├── AllJobs.jsx         # Browse all jobs page
│   ├── EditJob.jsx         # Edit job page
│   ├── Landing.jsx         # Landing page
│   ├── Login.jsx           # Login page
│   ├── Register.jsx        # Registration page
│   ├── Profile.jsx         # User profile page
│   └── [other pages]
├── Router/                  # Routing configuration
│   └── Routes.jsx          # Application routes
└── utils/                   # Utility functions
    ├── DashboardNavLinkData.jsx # Navigation data
    ├── FetchHandlers.js         # API fetch utilities
    └── JobData.js              # Job-related utilities
```

## Installation & Setup

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Running backend server

### Setup Instructions

1. **Navigate to the frontend directory:**

   ```bash
   cd full-stack-job-portal-client-main
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Environment Configuration (Optional):**
   Create a `.env` file in the root directory if you need to configure API endpoints:

   ```env
   VITE_API_URL=http://localhost:80
   ```

4. **Start the development server:**

   ```bash
   npm run dev
   ```

   The application will be available at `http://localhost:5173`

5. **Build for production:**

   ```bash
   npm run build
   ```

6. **Preview production build:**
   ```bash
   npm run preview
   ```

## Key Components

### Authentication Flow

- **Login/Register Pages** - User authentication interface
- **Protected Routes** - Route guards based on user roles
- **Authentication Context** - Global authentication state management

### Job Management

- **Job Cards** - Display job information in card format
- **Search & Filter** - Advanced job search functionality
- **Pagination** - Handle large datasets efficiently
- **Job Details** - Detailed job information pages

### Dashboard Components

- **Navigation** - Role-based navigation menus
- **Statistics** - Data visualization with charts
- **Forms** - Dynamic forms for job posting and editing
- **Tables** - Data tables for managing jobs and applications

### UI/UX Features

- **Loading States** - Skeleton screens and loading indicators
- **Error Handling** - User-friendly error messages
- **Notifications** - Success/error notifications with SweetAlert2

## API Integration

The frontend communicates with the backend through RESTful APIs using Axios:

```javascript
// Example API call structure
import axios from "axios";

const api = axios.create({
  baseURL: "http://localhost:80",
  withCredentials: true,
});

// Get all jobs
export const getAllJobs = async (params) => {
  const response = await api.get("/jobs", { params });
  return response.data;
};
```

## Troubleshooting

### Common Issues

1. **Port already in use:**

   ```bash
   # Kill process on port 5173
   lsof -ti:5173 | xargs kill -9
   ```

2. **Module not found errors:**

   ```bash
   # Clear node_modules and reinstall
   rm -rf node_modules package-lock.json
   npm install
   ```

3. **Build errors:**
   ```bash
   # Check for TypeScript errors
   npm run lint
   ```

## Support

For frontend-specific issues:

- Check the browser console for errors
- Verify API endpoints are accessible
- Ensure all environment variables are configured
- Review the component structure and routing

---

**Note:** Make sure the backend server is running before starting the frontend development server.
