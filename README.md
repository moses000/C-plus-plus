
# C++ Recommendation System

This is a recommendation system implemented in C++ using the Poco C++ Libraries for web development. It provides various recommendation endpoints for users based on different criteria.

## Features

- **Hybrid Recommendation**: Combines collaborative filtering and content-based filtering for recommendations.
- **User-Based Recommendations**: Provides recommendations based on user history and preferences.
- **General Recommendations**: Offers general recommendations based on popularity or other criteria.
- **Popular Products**: Lists the most popular products based on overall ratings.
- **New Products**: Displays recently added products based on timestamp.

## Prerequisites

- C++ compiler (supporting C++11)
- Poco C++ Libraries (installation instructions [here](https://pocoproject.org/docs/00200-GettingStarted.html))
- MongoDB or other database for storing product and purchase history data

## Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/your/repository.git
   cd repository
   ```

2. Build the project using the C++ compiler and link against the Poco libraries.

3. Configure the database connection in the source code (`main.cpp`) according to your setup.

## Usage

1. Start the server:

   ```sh
   ./RecommendationServer
   ```

2. Send HTTP POST requests to the following endpoints:

   - `/recommend`: Get recommendations for a known user.
   - `/general_recommend`: Get general recommendations for an unknown user.
   - `/user_history_recommend`: Get recommendations based on user purchase history.
   - `/user_preferences_recommend`: Get recommendations based on user preferences.
   - `/popular_products`: Get popular products.
   - `/new_products`: Get new products.

   Example request body for `/recommend` endpoint:

   ```json
   {
       "user_id": 123,
       "product_id": 456,
       "num_recommendations": 5
   }
   ```

3. Receive JSON responses with the recommendation results.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License 
