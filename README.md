# MERN E-Commerce Application

A full-stack e-commerce application built with the MERN stack (MongoDB, Express.js, React, Node.js). This project provides a complete online shopping experience with user authentication, product management, cart functionality, order processing, and admin dashboard.

## Features

### User Features
- User registration and login with OTP verification
- Password reset functionality
- Product browsing and search
- Shopping cart management
- Wishlist functionality
- Order placement and tracking
- User profile management
- Address management
- Product reviews and ratings

### Admin Features
- Admin dashboard with analytics
- Product management (add, update, delete)
- Order management
- User management
- Category and brand management

### Technical Features
- JWT-based authentication
- Secure payment processing
- Email notifications
- File upload for product images
- Responsive design
- Real-time updates

## Tech Stack

### Frontend
- React.js
- Redux Toolkit for state management
- React Router for navigation
- Material-UI for UI components
- Axios for API calls
- Lottie for animations

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- Nodemailer for emails
- Multer for file uploads
- bcrypt for password hashing

### Deployment
- Vercel for backend deployment
- Netlify for frontend deployment (optional)

## Project Structure

```
mern-ecommerce-main/
├── backend/
│   ├── controllers/     # Route controllers
│   ├── models/         # MongoDB models
│   ├── routes/         # API routes
│   ├── middleware/     # Custom middleware
│   ├── utils/          # Utility functions
│   ├── seed/           # Database seeding
│   ├── database/       # Database connection
│   ├── index.js        # Server entry point
│   └── package.json
├── frontend/
│   ├── public/         # Static assets
│   ├── src/
│   │   ├── components/ # Reusable components
│   │   ├── pages/      # Page components
│   │   ├── features/   # Redux slices and APIs
│   │   ├── hooks/      # Custom hooks
│   │   ├── config/     # Configuration files
│   │   ├── constants/  # App constants
│   │   ├── theme/      # Theme configuration
│   │   ├── App.js      # Main app component
│   │   └── index.js    # React entry point
│   └── package.json
├── .gitignore
├── package.json
└── README.md
```

## Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- Git

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the backend directory with the following variables:
   ```
   PORT=5000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   EMAIL_USER=your_email@gmail.com
   EMAIL_PASS=your_email_password
   CLOUDINARY_CLOUD_NAME=your_cloudinary_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   ```

4. Start the backend server:
   ```bash
   npm start
   ```

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the frontend directory:
   ```
   REACT_APP_API_URL=http://localhost:5000/api
   ```

4. Start the frontend development server:
   ```bash
   npm start
   ```

## Usage

1. Open your browser and navigate to `http://localhost:3000`
2. Register a new account or login with existing credentials
3. Browse products, add to cart, and place orders
4. Admin users can access the admin dashboard at `/admin`

## API Endpoints

### Authentication
- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/verify-otp` - OTP verification
- `POST /api/auth/forgot-password` - Forgot password
- `POST /api/auth/reset-password` - Reset password

### Products
- `GET /api/products` - Get all products
- `GET /api/products/:id` - Get product by ID
- `POST /api/products` - Create product (Admin)
- `PUT /api/products/:id` - Update product (Admin)
- `DELETE /api/products/:id` - Delete product (Admin)

### Cart
- `GET /api/cart` - Get user's cart
- `POST /api/cart` - Add item to cart
- `PUT /api/cart/:id` - Update cart item
- `DELETE /api/cart/:id` - Remove item from cart

### Orders
- `GET /api/orders` - Get user's orders
- `POST /api/orders` - Create new order
- `GET /api/orders/:id` - Get order by ID
- `PUT /api/orders/:id` - Update order status (Admin)

### Users
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or support, please contact the development team.

---

**Note:** This is a full-stack application. Make sure both backend and frontend servers are running for the complete functionality.
