
## About Contract Management Serverless

This project is a serverless PoC of contract management application that allow users to create and retrieve contracts.

## Getting Started

These instructions will give you a copy of the project up and running on
your local machine for development and testing purposes. You can run this project using docker
or you can set up your own local environment. 

### Docker installation

Make sure that you have docker up and running on your machine. Open a new terminal in the project
directory and build your docker image using this command:

    docker build . -t contract-management-serverless:latest

After that you can start the project by tying this command:

    docker run -it -p 3000:3000 contract-management-serverless

This command will start the serverless offline server listening on port 3000, and you can start make requests.

### Manual installation

Make sure that you have node js 16.x installed on your local machine as well as Java Runtime Environment.
Open a new terminal in the project directory and run this command to install dependencies:

    npm install

After that you need to initialize dynamo db local by typing this command:

    npm run dynamo

And finally you need to run this command to start the server:

    npm start

This command will start the serverless offline server listening on port 3000, and you can start make requests.



## Usage

This application implement three endpoints to manage contracts:

- Post `/createContract` create a new contract
- Get `/getContract` retrieve a contract by id
- Get `/getContractIDs` retrieve all contract ids

### API Key

Please note that this application is protected by a hardcoded API Key and you need to add an`Authorization` header
before sending any request, otherwise you will get `401 unauthorized` response. You can find the API Key value bellow:

    "Authorization": "lPpdaKwVw4Kv4FWJFxUTDXr9M5zFJfF4f6R9PT1u0ByxDEtMPogFO54Sb509G4WZ"


### Documentation

Detailed openAPI documentation is provided with all availble endpoints, request objects, response objects
and examples. You can find the documentation [here](./documentation/index.html).

### Unit tests

This project is tested with Jest testing framework. You can run all available tests using this command:

    npm test



