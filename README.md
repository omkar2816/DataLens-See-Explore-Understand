# 📊 DataLens: See, Explore & Understand

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![React](https://img.shields.io/badge/React-18.2.0-blue.svg)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18.0%2B-green.svg)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.0%2B-green.svg)](https://mongodb.com/)
[![Express.js](https://img.shields.io/badge/Express.js-4.18.2-lightgrey.svg)](https://expressjs.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9.2-blue.svg)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-5.0.0-646CFF.svg)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-3.3.6-38B2AC.svg)](https://tailwindcss.com/)

A comprehensive full-stack web application for uploading, analyzing, and visualizing Excel data with advanced chart generation capabilities including both 2D and 3D visualizations.

## Project Preview Video

<iframe
  width="560"
  height="315"
  src="https://www.youtube.com/embed/oj3CQgLs83A"
  title="DataLens Project Demo"
  allowfullscreen>
</iframe>

## 🌟 Features

### Core Functionality
- **📄 Excel File Upload**: Support for .xlsx, .xls, and .csv files
- **📊 Advanced Analytics**: Automated data analysis and insights generation
- **📈 Chart Generation**: Create beautiful 2D and interactive 3D charts
- **👥 Multi-User System**: Role-based access control (User, Admin, Super Admin)
- **🔐 Secure Authentication**: JWT-based authentication with password hashing
- **📱 Responsive Design**: Modern, mobile-friendly interface
- **🔔 Real-time Notifications**: Live updates and activity tracking
- **📈 Dashboard Analytics**: Comprehensive admin dashboard with user metrics

### Chart Types
- **2D Charts**: Bar, Line, Pie, Scatter, Area charts using Recharts
- **3D Charts**: Interactive 3D visualizations using Plotly.js and Three.js
- **Export Options**: PNG, PDF export functionality
- **Interactive Features**: Zoom, pan, hover tooltips, and data filtering

### User Roles
- **👤 User**: Upload files, create charts, view personal analytics
- **👨‍💼 Admin**: Manage users, view all activities, access analytics dashboard
- **👑 Super Admin**: Full system control, user role management, system settings

## 🏗️ Project Structure

```
excel-analytics-platform/
├── 📁 backend/                    # Node.js/Express API server
│   ├── 📁 middleware/             # Authentication & validation middleware
│   │   └── auth.js               # JWT authentication middleware
│   ├── 📁 models/                # MongoDB data models
│   │   ├── User.js               # User account model
│   │   ├── ChartHistory.js       # Chart storage model
│   │   ├── UploadedFile.js       # File metadata model
│   │   ├── Activity.js           # User activity tracking
│   │   ├── UserActivity.js       # Detailed user actions
│   │   ├── Notification.js       # System notifications
│   │   ├── AdminRequest.js       # Admin role requests
│   │   └── DatasetProcessingHistory.js # Processing logs
│   ├── 📁 routes/                # API route handlers
│   │   ├── auth.js               # Authentication routes
│   │   ├── users.js              # User management
│   │   ├── analytics.js          # Data analysis endpoints
│   │   ├── analyticsEnhanced.js  # Advanced analytics
│   │   ├── history.js            # Chart history management
│   │   ├── notifications.js      # Notification system
│   │   └── tabNotifications.js   # Tab-specific notifications
│   ├── 📁 services/              # Business logic services
│   │   ├── DataPreprocessor.js   # Data cleaning & processing
│   │   ├── SmartChartConfigurator.js # Intelligent chart configuration
│   │   └── NotificationService.js # Notification management
│   ├── 📁 utils/                 # Utility functions
│   │   ├── dataProcessing.js     # Data manipulation utilities
│   │   ├── activityLogger.js     # Activity tracking
│   │   ├── notificationEvents.js # Event handling
│   │   └── mailer.js             # Email functionality
│   ├── 📁 scripts/               # Database & maintenance scripts
│   ├── 📁 uploads/               # File upload storage
│   ├── .env.example              # Environment variables template
│   ├── server.js                 # Main server entry point
│   └── package.json              # Backend dependencies
├── 📁 frontend/                   # React.js client application
│   ├── 📁 src/                   # Source code
│   │   ├── 📁 components/        # Reusable UI components
│   │   ├── 📁 pages/             # Page components
│   │   ├── 📁 store/             # Redux state management
│   │   ├── 📁 config/            # Configuration files
│   │   ├── 📁 utils/             # Frontend utilities
│   │   ├── App.jsx               # Main app component
│   │   └── main.jsx              # Application entry point
│   ├── index.html                # HTML template
│   ├── vite.config.js            # Vite build configuration
│   ├── tailwind.config.ts        # Tailwind CSS configuration
│   └── package.json              # Frontend dependencies
├── .gitignore                    # Git ignore rules
└── README.md                     # Project documentation
```

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v18.0.0 or higher) - [Download here](https://nodejs.org/)
- **MongoDB** (v5.0 or higher) - [Download here](https://www.mongodb.com/try/download/community)
- **Git** - [Download here](https://git-scm.com/)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/omkar2816/Zidio-Dev-Project-1.git
   cd Zidio-Dev-Project-1
   ```

2. **Backend Setup**
   ```bash
   # Navigate to backend directory
   cd backend
   
   # Install dependencies
   npm install
   
   # Create environment file
   cp .env.example .env
   
   # Edit .env file with your configuration (see Environment Variables section)
   ```

3. **Frontend Setup**
   ```bash
   # Navigate to frontend directory (from project root)
   cd frontend
   
   # Install dependencies
   npm install
   ```

4. **Database Setup**
   ```bash
   # Start MongoDB service
   # On Windows: net start MongoDB
   # On macOS: brew services start mongodb-community
   # On Linux: sudo systemctl start mongod
   
   # The application will automatically create the database and collections
   ```

5. **Start the Application**
   
   **Backend (Terminal 1):**
   ```bash
   cd backend
   npm run dev
   ```
   
   **Frontend (Terminal 2):**
   ```bash
   cd frontend
   npm run dev
   ```

6. **Access the Application**
   - Frontend: http://localhost:5173
   - Backend API: http://localhost:5000
   - Default Super Admin: admin@datalens.local / Admin@123

## ⚙️ Environment Variables

### Backend Configuration (.env)

```bash
# Server Configuration
PORT=5000
NODE_ENV=development

# Database Configuration
MONGODB_URI=mongodb://127.0.0.1:27017/excelAnalytics

# JWT Secret (CHANGE THIS IN PRODUCTION!)
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production

# Default Admin Configuration
ADMIN_EMAIL=admin@datalens.local
ADMIN_PASSWORD=Admin@123
ADMIN_FIRST_NAME=Admin
ADMIN_LAST_NAME=User
ADMIN_FORCE_RESET=true

# SMTP Configuration (for sending OTP emails)
SMTP_HOST=your-smtp-host
SMTP_PORT=587
SMTP_USER=your-smtp-username
SMTP_PASS=your-smtp-password
SMTP_SECURE=false
```

### Environment Variable Descriptions

| Variable | Description | Default | Required |
|----------|-------------|---------|----------|
| `PORT` | Backend server port | 5000 | No |
| `NODE_ENV` | Environment mode | development | No |
| `MONGODB_URI` | MongoDB connection string | mongodb://127.0.0.1:27017/excelAnalytics | Yes |
| `JWT_SECRET` | Secret key for JWT tokens | - | Yes |
| `ADMIN_EMAIL` | Default admin email | admin@datalens.local | No |
| `ADMIN_PASSWORD` | Default admin password | Admin@123 | No |
| `ADMIN_FIRST_NAME` | Default admin first name | Admin | No |
| `ADMIN_LAST_NAME` | Default admin last name | User | No |
| `ADMIN_FORCE_RESET` | Force admin account reset | true | No |
| `SMTP_HOST` | SMTP server hostname | - | No* |
| `SMTP_PORT` | SMTP server port | 587 | No* |
| `SMTP_USER` | SMTP username | - | No* |
| `SMTP_PASS` | SMTP password | - | No* |
| `SMTP_SECURE` | Use secure connection | false | No* |

*Required for email functionality (OTP, notifications)

## 📖 User Manual

### 🔐 Authentication

#### For New Users:
1. **Registration**
   - Visit the application homepage
   - Click "Sign Up" or "Register"
   - Fill in required information (name, email, password)
   - Verify your email if SMTP is configured
   - Login with your credentials

2. **Login**
   - Enter email and password
   - Click "Login"
   - You'll be redirected to the dashboard

#### For Admins:
- Use the default admin credentials provided in the .env file
- Change the password after first login for security

### 📊 Using the Platform

#### 1. **File Upload**
   - Navigate to "Upload" section
   - Click "Choose File" or drag and drop
   - Supported formats: .xlsx, .xls, .csv
   - Maximum file size: 50MB
   - Wait for processing confirmation

#### 2. **Data Analysis**
   - After upload, view the "Analytics" dashboard
   - See data summary, column analysis, and statistics
   - Review data quality indicators
   - Check for missing values and data types

#### 3. **Chart Creation**
   - Go to "Charts" section
   - Select your uploaded dataset
   - Choose chart type (2D or 3D)
   - Configure chart options:
     - X-axis and Y-axis selection
     - Chart title and labels
     - Color schemes
     - Filters and grouping
   - Preview and save your chart

#### 4. **Chart Management**
   - View all your charts in "My Charts"
   - Edit chart configurations
   - Export charts as PNG or PDF
   - Share charts with other users (if admin)
   - Delete unwanted charts

#### 5. **Dashboard Features**
   - **Overview**: Quick stats and recent activity
   - **Analytics**: Detailed data insights
   - **History**: Track all your activities
   - **Notifications**: System updates and alerts

### 👨‍💼 Admin Features

#### User Management:
- View all registered users
- Manage user roles (User, Admin, Super Admin)
- Monitor user activities
- Deactivate/activate user accounts

#### System Analytics:
- Total users and usage statistics
- File upload trends
- Chart creation metrics
- System performance indicators

#### Content Management:
- View all uploaded files
- Monitor system storage usage
- Manage chart galleries
- System notifications and announcements

### 👑 Super Admin Features

#### Complete System Control:
- All admin features plus:
- System configuration management
- Database maintenance tools
- Advanced user role assignments
- System backup and restore options

## 🛠️ API Documentation

### Authentication Endpoints

```http
POST /api/auth/register
POST /api/auth/login
POST /api/auth/logout
GET  /api/auth/me
```

### User Management

```http
GET    /api/users/
POST   /api/users/
PUT    /api/users/:id
DELETE /api/users/:id
PUT    /api/users/:id/role
```

### Analytics & Charts

```http
POST   /api/analytics/upload
GET    /api/analytics/files
POST   /api/analytics/analyze
GET    /api/analytics/charts
POST   /api/analytics/charts
PUT    /api/analytics/charts/:id
DELETE /api/analytics/charts/:id
```

### Notifications

```http
GET    /api/notifications/
POST   /api/notifications/
PUT    /api/notifications/:id/read
DELETE /api/notifications/:id
```

## 🧪 Development

### Running in Development Mode

```bash
# Backend with auto-reload
cd backend
npm run dev

# Frontend with hot-reload
cd frontend
npm run dev
```

### Building for Production

```bash
# Build frontend
cd frontend
npm run build

# Start backend in production mode
cd backend
npm start
```

### Database Scripts

```bash
# Create super admin
node backend/createSuperAdmin.js

# Cleanup users
node backend/cleanupUsers.js

# Migrate files to MongoDB
npm run migrate-files
```

## 🔧 Troubleshooting

### Common Issues

1. **Database Connection Error**
   - Ensure MongoDB is running
   - Check MONGODB_URI in .env
   - Verify network connectivity

2. **File Upload Fails**
   - Check file format (.xlsx, .xls, .csv)
   - Verify file size (<50MB)
   - Ensure uploads directory exists and is writable

3. **Charts Not Rendering**
   - Check browser console for JavaScript errors
   - Ensure data is properly formatted
   - Verify chart configuration parameters

4. **Authentication Issues**
   - Check JWT_SECRET in .env
   - Clear browser localStorage
   - Verify token expiration settings

5. **Email/SMTP Issues**
   - Verify SMTP configuration in .env
   - Check firewall settings
   - Test SMTP credentials separately

### Performance Optimization

1. **Database Indexing**
   - MongoDB automatically creates indexes for common queries
   - Consider additional indexes for large datasets

2. **File Storage**
   - Regular cleanup of temporary files
   - Consider cloud storage for production

3. **Frontend Optimization**
   - Build optimization is handled by Vite
   - Consider lazy loading for large datasets

## 🔐 Security

### Security Features
- Password hashing with bcrypt
- JWT token authentication
- CORS protection
- Helmet.js security headers
- Input validation and sanitization
- File upload restrictions

### Security Best Practices
1. Change default admin credentials
2. Use strong JWT_SECRET in production
3. Enable HTTPS in production
4. Regularly update dependencies
5. Monitor file upload sizes
6. Implement rate limiting for API calls

## 🚀 Deployment

### Production Deployment

1. **Environment Setup**
   ```bash
   NODE_ENV=production
   JWT_SECRET=your-production-secret-key
   MONGODB_URI=mongodb://your-production-db
   ```

2. **Build Application**
   ```bash
   cd frontend
   npm run build
   ```

3. **Start Services**
   ```bash
   cd backend
   npm start
   ```

### Docker Deployment (Optional)

```dockerfile
# Example Dockerfile for backend
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
COPY . .
EXPOSE 5000
CMD ["npm", "start"]
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License.

## 🆘 Support

For support and questions:
- Create an issue on GitHub
- Contact the development team
- Check the troubleshooting section above

## 🙏 Acknowledgments

- **React.js** - Frontend framework
- **Node.js & Express** - Backend framework
- **MongoDB** - Database
- **Plotly.js** - 3D chart visualizations
- **Recharts** - 2D chart library
- **Three.js** - 3D graphics
- **Tailwind CSS** - Styling framework

----

**Made by the Omkar Korgaonkar**

> 🌟 **Star this repository if you found it helpful!**

**Happy Analyzing! 📊✨**
