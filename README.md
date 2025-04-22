
# Backend - FitFlow App

📘 Disponible también en [Español](./README.es.md)


## Overview

FitFlow App is an AI-powered agent that helps users discover and get personalized workout recommendations. It uses a RAG (Retrieval-Augmented Generation) architecture with Upstash to optimize storage and semantic retrieval of workout.

The backend is built with TypeScript and Node.js, and interfaces with a MongoDB database to manage user profiles and workout data. Integrates OpenAI’s API to enable a conversational AI assistant for user interactions.

## Technologies

-  **Node.js**: JavaScript runtime environment.
-  **TypeScript**: Language that builds on JavaScript
-  **MongoDB**: NoSQL database for storing users and exercises.
-  **Upstash**: RAG-based vector DB for fast semantic search.
-  **OpenAI API**: API KEY para poder utilizar el chat y consultar datos.
-  **Jest**: Testing framework for backend and route logic

## Key Features

-  **Authentication**: User management with JWT.
-  **Exercise Recommendation**: Personalized search and suggestions.
-  **AI Chat Assistant**: Natural language interaction for workout guidance, saved directly to the user profile.
-  **RAG Integration**: Uses Upstash to optimize speed and accuracy in exercise-related queries.

## Project Structure

```
backend/

├── docs/ # API documentation (Swagger)

├── src/ # Main source code

│ ├── api/ # Controllers, routes, middlewares

│ ├── config/ # App configuration

│ ├── constants/ # Global constants

│ ├── interfaces/ # TypeScript interfaces

│ ├── models/ # Data models

│ ├── responses/ # Standardized API responses  

│ ├── schemas/ # Validation schemas

│ ├── services/ # Business logic

│ ├── tests/ # Unit and integration tests

│ ├── utils/ # Utility functions

├── package.json # Dependencies and scripts

├── tsconfig.json # TypeScript config

```

## Prerequisites

- Node.js (v16 o +)

- npm

## Setup

1. Clone the repository:

	```bash
	git clone https://github.com/nuriadevs/backend-api-fitflow
	cd backend-api-fitflow
	```

2. Install dependencies:

	```bash
	npm install
	```

  

## Scripts

-  `npm start`: Starts the server in development mode with nodemon.

-  `npm test`: Runs tests using Jest.

## Environment Variables

  

1. Create a `.env` file in the root directory and define the following variables:

  

	```env

	DATABASE_URL=<DATABASE_URL>

	JWT_SECRET=<JWT_SECRET>

	OPENAI_API_KEY=<YOUR_OPENAI_API_KEY>

	MONGODB_URI=<MONGODB_CONNECTION_URI>

	PORT=<SERVER_PORT>

	CORS_ORIGIN=<ALLOWED_ORIGIN>

	NODE_ENV=<ENVIRONMENT>

	UPSTASH_VECTOR_REST_URL=<VECTOR_REST_URL>

	UPSTASH_VECTOR_REST_TOKEN=<UPSTASH_TOKEN>

	```

  

2. You can customize additional settings in `src/config/env.ts` as needed.

  

## API Documentation

API docs are available in `docs/swagger.yaml`. You can preview them using Swagger UI or import into Postman,  Bruno,etc... .

## Testing

Run tests with:

```bash
npm test
```

## Chat requests
You can send chat requests using the following examples:
- Recommend exercises for biceps.
- Recommend exercises for triceps.
- Recommend a routine for training glutes.


## Demo

![backend api](media/backend-api/backend-api.jpg)




[Watch video demo backend](https://youtu.be/7JgR5SAsv9U)


## Links 
- [OpenAI](https://platform.openai.com/docs/overview)
- [UpStash](https://upstash.com/)
- [MongoDB](https://www.mongodb.com/)


## Summary

-   Don't forget to create your own .env file for the variables.
-   This project is under construction...can be improved.
