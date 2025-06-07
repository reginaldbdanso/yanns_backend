# Yanns Backend

Yanns Backend is a robust Node.js/Express API powering the Yanns Tech Hub platform. It provides secure, scalable endpoints for product management, user authentication, orders, reviews, payments, wishlists, and more.

## Features

- **User Authentication & Profiles**: Secure JWT-based auth, user profile management.
- **Product Management**: CRUD operations for products, categories, and inventory.
- **Order Processing**: Cart, checkout, and order management with multiple shipping/payment methods.
- **Reviews & Ratings**: Product reviews and ratings by authenticated users.
- **Wishlist**: Add/remove products to user wishlists.
- **Payment Integration**: Payment method management and simulated payment processing.
- **Data Seeding**: Populate the database with sample products and reviews for development/testing.
- **Security**: Helmet, CORS, and environment-based configuration.

## Tech Stack

- Node.js, Express.js
- MongoDB (via Mongoose)
- JWT for authentication
- Multer for file uploads
- Cloudinary/Google Drive for media storage
- dotenv for environment management

## Getting Started

### Prerequisites

- Node.js (v18+ recommended)
- MongoDB Atlas or local MongoDB instance
- npm

### Installation

```bash
git clone <your-repo-url>
cd yanns_backend
npm install
```

### Environment Variables

Create a `.env` file in the root directory with the following keys:

```
MONGODB_CONNECTION_STRING=your_mongodb_uri
PORT=4000
NODE_ENV=development
JWT_SECRET=your_jwt_secret
CLOUDINARY_API_KEY=your_cloudinary_key
CLOUDINARY_API_SECRET=your_cloudinary_secret
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud
```

### Running the Server

- **Development**: `npm run dev`
- **Production**: `npm start`

The server runs on `http://localhost:4000` by default.

### API Endpoints

| Resource   | Endpoint Prefix      | Description                |
|------------|---------------------|----------------------------|
| Auth       | `/api/auth`         | Register, login, profile   |
| Products   | `/api/products`     | Product CRUD, details      |
| Orders     | `/api/orders`       | User orders, admin orders  |
| Cart       | `/api/cart`         | Cart management            |
| Reviews    | `/api/reviews`      | Product reviews            |
| Checkout   | `/api/checkout`     | Shipping, order creation   |
| Payment    | `/api/payment`      | Payment methods, process   |
| Wishlist   | `/api/wishlist`     | User wishlists             |
| Profile    | `/api/profile`      | User profile management    |

### Data Seeding

To seed the database with sample data (products, reviews, etc.), the server will automatically run the seeding script in development mode.

### Project Structure

```
controllers/   # Route handlers
models/        # Mongoose schemas
routes/        # Express route definitions
services/      # Business logic
middleware/    # Auth, error handling, etc.
utils/         # Data seeding, helpers
config/        # DB and cloud config
```

### Scripts

- `npm run dev` — Start server with nodemon (auto-reload)
- `npm start` — Start server in production mode

### License

This project is licensed under the ISC License.