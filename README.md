## Pizza Restaurants Tracker API
This is a mini Rails application that tracks pizza restaurants. It provides a RESTful API for managing restaurants, pizzas, and restaurant pizzas.

### Getting Started
To get started with the project, follow these steps:

1. Clone this repository to your local machine.
2. Install the required dependencies by running bundle install.
3. Run the database migrations with rails db:migrate.
4. Seed the database with sample data by running rails db:seed.

### Models
The following relationships are established in the application:

A Restaurant has many Pizzas through RestaurantPizza
A Pizza has many Restaurants through RestaurantPizza
A RestaurantPizza belongs to a Restaurant and belongs to a Pizza
Validations
The RestaurantPizza model has a validation to ensure that the price is between 1 and 30.

### Routes
The following routes are available:

#### GET /restaurants
Returns an array of all restaurants with their name, address, and id.

#### GET /restaurants/:id
Returns a specific restaurant with the given id, including an array of its pizzas. If the restaurant is not found, returns an error message.

#### DELETE /restaurants/:id
Deletes the restaurant with the given id and all associated restaurant pizzas. If the restaurant is not found, returns an error message.

#### GET /pizzas
Returns an array of all pizzas with their name, ingredients, and id.

#### POST /restaurant_pizzas
Creates a new restaurant pizza record with the provided pizza_id, restaurant_id, and price. If successful, returns the pizza details. If not successful, returns an array of error messages.

## Contributors
Lucy NJambi Muhoro - 
This project was created as part of an assessment for Flatiron School And Moringa School
