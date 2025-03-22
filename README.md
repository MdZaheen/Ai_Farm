# Farmers Assistance Application

A comprehensive platform to assist farmers with crop information, weather data, market prices, and expert advice.

## Features

- **User Authentication**: Register and login for farmers, agricultural experts, and administrators.
- **Crop Information**: Detailed information about various crops, including growing seasons, soil requirements, diseases, and treatments.
- **Weather Data**: Location-based weather information and forecasts to help farmers plan their activities.
- **Market Prices**: Real-time market prices for different crops across various markets.
- **Query System**: Platform for farmers to ask questions and receive answers from agricultural experts.
- **Image Analysis**: Upload images of crops/plants to identify diseases and get treatment recommendations.

## Tech Stack

- **Frontend**: Next.js, React, TypeScript, Tailwind CSS
- **Backend**: Next.js API Routes
- **Database**: MongoDB with Mongoose
- **Authentication**: JWT (JSON Web Tokens)
- **Image Processing**: TensorFlow.js (for plant disease detection)

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- MongoDB (local or Atlas)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/farmers-assistance.git
   cd farmers-assistance
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env.local` file in the root directory with the following variables:
   ```
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   JWT_EXPIRES_IN=30d
   ```

4. Run the development server:
   ```bash
   npm run dev
   ```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login a user
- `POST /api/auth/logout` - Logout a user
- `GET /api/auth/me` - Get current user

### Crops
- `GET /api/crops` - Get all crops
- `POST /api/crops` - Add a new crop (experts and admins only)
- `GET /api/crops/:id` - Get a specific crop
- `PUT /api/crops/:id` - Update a crop (experts and admins only)
- `DELETE /api/crops/:id` - Delete a crop (admins only)

### Queries
- `GET /api/queries` - Get all queries
- `POST /api/queries` - Add a new query
- `GET /api/queries/:id` - Get a specific query
- `PUT /api/queries/:id` - Update a query (only the user who asked it)
- `DELETE /api/queries/:id` - Delete a query (only the user who asked it or admin)
- `POST /api/queries/:id/answers` - Add an answer to a query
- `PUT /api/queries/:id/answers/:answerId/accept` - Accept an answer (only the user who asked the query)

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- [Next.js](https://nextjs.org/)
- [MongoDB](https://www.mongodb.com/)
- [Mongoose](https://mongoosejs.com/)
- [Tailwind CSS](https://tailwindcss.com/)
- [JWT](https://jwt.io/)
#   A i _ F a r m  
 