# BookReview Platform 📚

A modern, full-stack book review platform built with React and Node.js, featuring user authentication, book management, review systems, and a beautiful responsive design.

![BookReview Platform](https://images.pexels.com/photos/1082899/pexels-photo-1082899.jpeg?auto=compress&cs=tinysrgb&w=800)

## 🌟 Features

### Frontend Features
- **Modern React UI** with TypeScript and Tailwind CSS
- **Responsive Design** optimized for mobile, tablet, and desktop
- **User Authentication** with login/register functionality
- **Advanced Book Search** with real-time filtering by genre, author, and title
- **Interactive Book Cards** with ratings, reviews, and hover effects
- **Detailed Book Pages** with comprehensive information and review sections
- **User Profiles** with review history and statistics
- **Review System** with 5-star ratings and rich text content
- **Loading States** and error handling throughout the application
- **Smooth Animations** and micro-interactions for enhanced UX

### Backend Features
- **RESTful API** built with Express.js
- **JWT Authentication** for secure user sessions
- **Data Validation** using express-validator
- **Rate Limiting** to prevent API abuse
- **CORS Support** for cross-origin requests
- **Error Handling** middleware with detailed error responses
- **Mock Database** with realistic sample data
- **Admin Features** for book management
- **Review Management** with CRUD operations

## 🚀 Tech Stack

### Frontend
- **React 18** with TypeScript
- **React Router DOM** for navigation
- **Tailwind CSS** for styling
- **Lucide React** for icons
- **Context API** for state management
- **Vite** for development and building

### Backend
- **Node.js** with Express.js
- **JWT** for authentication
- **bcryptjs** for password hashing
- **express-validator** for input validation
- **express-rate-limit** for API protection
- **CORS** for cross-origin support
- **Concurrently** for running multiple processes

## 📋 Prerequisites

Before running this project, make sure you have the following installed:

- **Node.js** (version 16.0 or higher)
- **npm** (version 7.0 or higher)
- **Git** (for cloning the repository)

## 🛠️ Installation & Setup

### 1. Clone the Repository
```bash
git clone <repository-url>
cd book-review-platform
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Environment Setup
The application uses mock data by default, so no additional environment setup is required for development. However, you can configure the following environment variables if needed:

Create a `.env` file in the root directory:
```env
# Server Configuration
PORT=3001
NODE_ENV=development

# JWT Configuration
JWT_SECRET=your-super-secret-jwt-key-here

# Database Configuration (for future Supabase integration)
SUPABASE_URL=your-supabase-url
SUPABASE_ANON_KEY=your-supabase-anon-key
```

## 🏃‍♂️ Running the Application

### Development Mode
Start both frontend and backend servers concurrently:
```bash
npm run dev
```

This command will:
- Start the React development server on `http://localhost:5173`
- Start the Express backend server on `http://localhost:3001`
- Enable hot reloading for both frontend and backend

### Individual Server Commands

#### Frontend Only
```bash
npm run dev:client
```

#### Backend Only
```bash
npm run dev:server
```

### Production Build
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

## 🔗 API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/me` - Get current user profile

### Books
- `GET /api/books` - Get all books (with pagination and filters)
- `GET /api/books/featured` - Get featured books
- `GET /api/books/:id` - Get specific book
- `POST /api/books` - Create new book (admin only)
- `PUT /api/books/:id` - Update book (admin only)
- `DELETE /api/books/:id` - Delete book (admin only)

### Reviews
- `GET /api/reviews` - Get all reviews (optionally filtered by book)
- `POST /api/reviews` - Create new review
- `PUT /api/reviews/:id` - Update review (own reviews only)
- `DELETE /api/reviews/:id` - Delete review (own reviews or admin)

### Users
- `GET /api/users/:id` - Get user profile
- `PUT /api/users/:id` - Update user profile

## 👤 Demo Accounts

### Regular User
- **Email:** demo@bookreview.com
- **Password:** demo123

### Admin User
- **Email:** admin@bookreview.com
- **Password:** admin123

## 📱 Application Structure

```
book-review-platform/
├── public/                 # Static assets
├── src/                   # Frontend source code
│   ├── components/        # Reusable React components
│   │   ├── Books/        # Book-related components
│   │   ├── Common/       # Shared components
│   │   ├── Layout/       # Layout components
│   │   └── Reviews/      # Review-related components
│   ├── contexts/         # React Context providers
│   ├── pages/            # Page components
│   │   └── Auth/         # Authentication pages
│   ├── services/         # API service functions
│   ├── types/            # TypeScript type definitions
│   └── App.tsx           # Main App component
├── server/               # Backend source code
│   ├── database/         # Database configuration and mock data
│   ├── middleware/       # Express middleware
│   ├── routes/           # API route handlers
│   └── index.js          # Server entry point
└── README.md            # Project documentation
```

## 🎨 Design Features

### Color Palette
- **Primary:** Blue gradient (#1E40AF to #7C3AED)
- **Secondary:** Purple accents
- **Success:** Green (#059669)
- **Warning:** Orange (#EA580C)
- **Error:** Red (#DC2626)
- **Neutral:** Gray scale

### Typography
- **Headings:** Bold, hierarchical sizing
- **Body:** Clean, readable fonts
- **Interactive:** Hover states and transitions

### Responsive Breakpoints
- **Mobile:** < 768px
- **Tablet:** 768px - 1024px
- **Desktop:** > 1024px

## 🔧 Development Guidelines

### Code Style
- **TypeScript** for type safety
- **ESLint** for code linting
- **Prettier** for code formatting
- **Component-based** architecture
- **Functional components** with hooks

### State Management
- **React Context** for global state
- **useState/useEffect** for local state
- **Custom hooks** for reusable logic

### API Integration
- **Centralized API service** in `src/services/api.ts`
- **Error handling** with try-catch blocks
- **Loading states** for better UX
- **JWT tokens** for authentication

## 🚀 Deployment

### Frontend Deployment
The frontend can be deployed to platforms like:
- **Vercel** (recommended for React apps)
- **Netlify**
- **GitHub Pages**

Build command: `npm run build`
Output directory: `dist`

### Backend Deployment
The backend can be deployed to:
- **Heroku**
- **Railway**
- **DigitalOcean App Platform**
- **AWS EC2**

Start command: `node server/index.js`

## 🔮 Future Enhancements

### Planned Features
- **Real Database Integration** with Supabase/PostgreSQL
- **Book Recommendations** based on user preferences
- **Reading Lists** and bookmarks
- **Social Features** (follow users, activity feeds)
- **Advanced Search** with filters and sorting
- **Book Categories** and genre management
- **Email Notifications** for new reviews
- **Mobile App** with React Native
- **Admin Dashboard** with analytics
- **Book Import** from external APIs (Google Books, OpenLibrary)

### Technical Improvements
- **Unit Testing** with Jest and React Testing Library
- **E2E Testing** with Cypress
- **Performance Optimization** with React.memo and useMemo
- **SEO Optimization** with React Helmet
- **PWA Features** for offline functionality
- **Docker Containerization** for easy deployment
- **CI/CD Pipeline** with GitHub Actions

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **React Team** for the amazing framework
- **Tailwind CSS** for the utility-first CSS framework
- **Lucide** for the beautiful icons
- **Pexels** for the stock images
- **Express.js** for the robust backend framework

## 📞 Support

If you have any questions or need help with the project, please:

1. Check the existing issues on GitHub
2. Create a new issue with detailed information
3. Contact the development team

---

**Happy Reading! 📖✨**