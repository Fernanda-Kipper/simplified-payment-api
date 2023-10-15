# Authentication API

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)

This project is an API built using **Java, Java Spring, H2 as the database.** 

The API was developed for my [Youtube Tutorial](https://www.youtube.com/watch?v=QXunBiLq2SM), to demonstrate how  to solve the [PicPay Backend Challenge](https://github.com/PicPay/picpay-desafio-backend) using Java Spring.
The Unit tests was developed during another [Youtube Tutorial](https://youtu.be/T6ChO8LQxRE), with the aim to demonstrate how to write unit tests for Java Spring apps using JUnit, Mockito and AssertJ.

## Table of Contents

- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Database](#database)
- [Contributing](#contributing)

## Installation

1. Clone the repository:

```bash
git clone https://github.com/Fernanda-Kipper/auth-api.git
```

2. Install dependencies with Maven

## Usage

1. Start the application with Maven
2. The API will be accessible at http://localhost:8080


## API Endpoints
The API provides the following endpoints:

```json
GET /users - Retrieve a list of all users. 

RESPONSE EXAMPLE:
[
    {
        "id": 1,
        "firstName": "Pedro",
        "lastName": "Silva",
        "document": "123456787",
        "email": "pedro@example.com",
        "password": "senha",
        "balance": 20.00,
        "userType": "MERCHANT"
    },
    {
        "id": 4,
        "firstName": "Luckas",
        "lastName": "Silva",
        "document": "123456783",
        "email": "luckas@example.com",
        "password": "senha",
        "balance": 0.00,
        "userType": "COMMON"
    }
]
```

```json
POST /transactions - Register a new Transaction between users (COMMON to COMMON or COMMON to MERCHANT)

REQUEST EXAMPLE:

{
  "senderId": 4,
  "receiverId": 1,
  "value": 10
}
```

```json
POST /users - Register a new user into the App

REQUEST EXAMPLE:
{
    "firstName": "Lucas",
    "lastName": "Silva",
    "password": "senha",
    "document": "123456783",
    "email": "lucas@example.com",
    "userType": "COMMON",
    "balance": 10
}
```

## Database
The project utilizes [H2 Database](https://www.h2database.com/html/tutorial.html) as the database. 

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request to the repository.

When contributing to this project, please follow the existing code style, [commit conventions](https://www.conventionalcommits.org/en/v1.0.0/), and submit your changes in a separate branch.




