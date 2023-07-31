# conversation-exporter-MERN-app
Personal learning project

Software Requirements Specification for MERN Stack Application
1. Introduction
The software system is a web application based on the MERN stack (MongoDB, Express.js, React.js, Node.js). The system will be containerized using Docker and will follow best practices for a professional development workflow.

Functions:

File Upload Module: Users should be able to upload their conversations.json file. This module will handle parsing the JSON object into discrete conversations and storing them in the database. The module will also handle uploading the file to the server and storing it in the file system. The module will be implemented as a REST API endpoint that accepts a POST request with the conversations.json file as the request body. # TODO add security and authentication to this module

Data Processing and Visualization Module: This module will parse the uploaded JSON file, process the data, and provide various visualization options. Visualizations could include things like a UI for reading and interacting with the conversations, a word cloud of the most common words, or a graph of the most common topics. Various descriptive statistics, etc. # TODO flesh out this module more

Conversation Viewer Module: This module will allow users to browse their conversations in an easy-to-read format. This could also include features like highlighting searchedpwd-for words or phrases, or tagging identified entities or topics.


Conversation Analysis Module: This module will provide more in-depth analysis of the conversations. Features might include topic modeling to identify common themes, named entity recognition to identify people, places, and organizations mentioned, or even a machine learning model to predict the sentiment or emotional tone of a conversation. #TODO develop more use cases for extracting value from the conversations

Search and Filtering: Users should be able to search their conversations for specific words or phrases. They should also be able to filter their conversations by criteria such as date, length, sentiment, or identified topics. We should aim for high levels of customization and flexibility in the search and filtering options.

User Account & Security: This would allow users to save their upload history, preferences, and custom visualizations or filters.

Data Export: users should be able to export their data all at once or subsets based on filtering, etc. We also want to be able to connect to other services and APIs to export data to other services like Google Sheets, etc. This should be a REST API endpoint that accepts a GET request with the desired export format as a query parameter.

API Documentation : As the complexity of the application grows, especially with the addition of more advanced analysis features, maintaining comprehensive and up-to-date API documentation will become increasingly important. This module will use Swagger to provide a clear, interactive documentation of the application's API.

2. System Overview
The system is divided into the following components:

Server-side: A Node.js application using Express.js as the web application framework. The application will be written in TypeScript and will utilize environment variables for configuration and sensitive data.
Client-side: A React.js application created using Create React App. The application will also be written in TypeScript for static type checking.
Database: MongoDB as the NoSQL database. Mongoose will be used for handling database migrations.
The entire application will be containerized using Docker, and Docker Compose will be used to manage the different Docker containers for the application.

3. System Configuration and Dependencie
The system requires the following dependencies and configuration:

Node.js and npm: The Node.js runtime and npm package manager are required for running the server-side application and managing its dependencies.
Docker: Docker is required for building and running the application containers.
TypeScript: TypeScript is used for static type checking in both the server-side and client-side applications.
ESLint and Prettier: ESLint is used for linting the JavaScript and TypeScript code, while Prettier is used for code formatting. Husky is used to enforce linting and formatting checks before commits.
Jest: Jest is used as the testing framework for the server-side and client-side applications.
Mongoose: Mongoose is used as the MongoDB object modeling tool and for handling database migrations.
Swagger: Swagger is used for API documentation.
4. System Setup and Initialization
The system setup and initialization involves the following steps:

Environment Setup: Setup the development environment with Node.js, npm, and Docker.
Project Initialization: Initialize the server-side and client-side projects and install their dependencies. This includes Express.js for the server-side and Create React App for the client-side.
Docker Configuration: Create Dockerfiles for the server-side and client-side applications and a docker-compose.yml file for managing the application containers.
TypeScript Configuration: Configure TypeScript for both the server-side and client-side applications.
ESLint, Prettier, and Husky Configuration: Configure ESLint and Prettier for linting and formatting, and setup Husky for pre-commit checks.
Jest Configuration: Configure Jest for testing both the server-side and client-side applications.
Mongoose Configuration: Configure Mongoose for MongoDB object modeling and handling database migrations.
Swagger Configuration: Configure Swagger for API documentation.
System Testing: Unit and Integration Testing
The system will utilize unit and integration testing to ensure the quality of the codebase and to prevent bugs and regressions. The server-side and client-side applications will be tested using Jest.