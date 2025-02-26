# World Capital Quiz

A web application that quizzes users on the capitals of various countries. The app fetches data from a PostgreSQL database and displays a random country for the user to guess its capital.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The World Capital Quiz is a web application that allows users to test their knowledge of world capitals. The app fetches data from a PostgreSQL database and displays a random country for the user to guess its capital. The user's score is tracked and displayed after each guess.

## Features

- Select a random country and guess its capital
- Fetch real-time data from a PostgreSQL database
- Track and display the user's score
- User-friendly interface

## Installation

To get started with the project, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/world-capital-quiz.git
    ```

2. Navigate to the project directory:
    ```sh
    cd world-capital-quiz
    ```

3. Install the dependencies:
    ```sh
    npm install
    ```

4. Set up the PostgreSQL database:
    - Ensure you have PostgreSQL installed and running.
    - Create a database named `world`.
    - Create a table named `capitals` with the following structure:
      ```sql
      CREATE TABLE capitals (
          id SERIAL PRIMARY KEY,
          country VARCHAR(255) NOT NULL,
          capital VARCHAR(255) NOT NULL
      );
      ```
    - Insert data into the `capitals` table.

5. Update the database configuration in [index.js](http://_vscodecontentref_/0):
    ```javascript
    const db = new pg.Client({
      user: "your-username",
      host: "localhost",
      database: "world",
      password: "your-password",
      port: 5432,
    });
    ```

## Usage

To start and run the app, follow these steps:

1. Start the server:
    ```sh
    npm start
    ```

2. Open your web browser and navigate to:
    ```
    http://localhost:3000
    ```

## Technologies Used

- Node.js
- Express.js
- EJS (Embedded JavaScript)
- PostgreSQL
- Axios
- HTML
- CSS

## Contributing

Contributions are welcome! If you would like to contribute to this project, please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add some feature'`)
5. Push to the branch (`git push origin feature-branch`)
6. Open a pull request

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.