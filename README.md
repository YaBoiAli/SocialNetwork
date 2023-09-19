# Social Network API

The Social Network API is a backend application that provides various routes and functionalities for managing users, thoughts, reactions, and friends within a social network platform. This README will guide you through the installation, usage, and available endpoints of the API.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Routes](#api-routes)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Installation

To run the Social Network API on your local machine, follow these steps:

1. Clone the repository to your local machine.

2. Navigate to the project directory.

3. Install the required dependencies.

4. Configure the MongoDB connection by updating the `.env` file with your MongoDB URI.

5. Start the server.

Your server should now be running, and the Mongoose models will be synced to the MongoDB database.

## Usage

### Testing the API

You can use a tool like [Insomnia](https://insomnia.rest/) or [Postman](https://www.postman.com/) to interact with the API. 

1. Open Insomnia or your preferred API testing tool.

2. Import the provided Insomnia workspace or manually create requests for the available API routes.

3. Use the following API routes to interact with the application.

## API Routes

### Users

- GET /api/users: Retrieve a list of all users.
- GET /api/users/:userId: Retrieve a specific user by ID.
- POST /api/users: Create a new user.
- PUT /api/users/:userId: Update a user by ID.
- DELETE /api/users/:userId: Delete a user by ID.

### Thoughts

- GET /api/thoughts: Retrieve a list of all thoughts.
- GET /api/thoughts/:thoughtId: Retrieve a specific thought by ID.
- POST /api/thoughts: Create a new thought.
- PUT /api/thoughts/:thoughtId: Update a thought by ID.
- DELETE /api/thoughts/:thoughtId: Delete a thought by ID.

### Reactions

- POST /api/thoughts/:thoughtId/reactions: Add a reaction to a thought.
- DELETE /api/thoughts/:thoughtId/reactions/:reactionId: Remove a reaction from a thought.

### Friends

- POST /api/users/:userId/friends/:friendId: Add a user as a friend to another user.
- DELETE /api/users/:userId/friends/:friendId: Remove a friend from a user's friend list.

## Examples

Here are some example requests for the API:

**Creating a User:**

POST /api/users
Content-Type: application/json

{
  "username": "johndoe",
  "email": "johndoe@example.com"
}

**Updating a Thought:**

PUT /api/thoughts/:thoughtId
Content-Type: application/json

{
  "text": "Updated thought content"
}

**Adding a Reaction to a Thought:**

POST /api/thoughts/:thoughtId/reactions
Content-Type: application/json

{
  "reactionBody": "Like"
}

**Adding a Friend:**

POST /api/users/:userId/friends/:friendId

## Contributing

Contributions to this project are welcome. To contribute, please follow these steps:

1. Fork the repository.

2. Create a new branch for your feature or bug fix.

3. Make your changes and test them.

4. Commit your changes.

5. Push your changes to your fork.

6. Create a pull request to the original repository.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
