# Introdução a APIs

[Fonte](https://blog.postman.com/what-is-an-api-endpoint/) desta sessão.

---

## What is an API endpoint?

Is a URL that acts as the point of contact between an API client and an API server.

API Clients -> Send requests to API endpoints
*in order to access the API’s functionality and data

A typical REST API has many endpoints that correspond to its available resources. For instance, an API that powers a social media application would likely include endpoints for users, posts, and comments. 

Requests to API endpoints must include a method, which indicates the operation to be performed, as well as the necessary headers, parameters, authentication credentials, and body data.

## How do API endpoints work?

API endpoints work by connecting API clients and servers—and handling the transfer of data between them. **A well-designed API should have clear and intuitive endpoints that provide a predictable way for clients to interact with the server’s resources**.

For example:
which can be accessed with the indicated HTTP methods:

- `/authors` – to retrieve a list of users (GET) or create a new user (POST)
- `/authors/:id` – to retrieve a specific user (GET), update an existing user (PUT or PATCH), or delete a specific user (DELETE)
- `/articles` –  to retrieve a list of articles (GET) or create a new article (POST)
- `/articles/:id` – to retrieve a specific article (GET), update an existing article (PUT or PATCH), or delete a specific article (DELETE)

The API client is responsible for assembling and sending the request to the API server. In addition to the endpoint and method, which are required, the request may also include parameters, HTTP headers, and a request body. 

Let’s explore those request components a little further:

- **Parameters** are variables that are passed to an API endpoint, and they provide specific instructions for the API to process. 

- **Request headers** are key-value pairs that provide additional information about the request. For instance, the Accept header specifies the media types that the client can accept, while the Authorization header is used to send tokens and API keys to authenticate the client.

- A **request body** includes the actual data that is required to create, update, or delete a resource. For instance, if an author wants to create a new article in our example blogging application, they would send a POST request to the /articles endpoint with the content of the article in the request’s body.

Once the client sends the request to the appropriate endpoint, the API server authenticates it, validates the input, retrieves or manipulates the relevant data, and returns the response to the client.

---

## What are some best practices for designing and developing API endpoints?

- Create a predictable and intuitive API endpoint structure
- Implement secure authentication mechanisms
- Validate and sanitize input data
- Clearly document every API endpoint
- Continually test and monitor your API endpoints

---

## What is the difference between a REST endpoint and a GraphQL endpoint?

This article has used REST API endpoints as examples because REST is the most commonly used API architecture today. However, there are many other API architectures and protocols, including GraphQL, which is an open source query language for APIs.

REST APIs include many endpoints that return fixed data structures, which can require the client to chain multiple requests together in order to obtain the exact data it needs. In contrast, GraphQL enables clients to interact with a single endpoint and specify the exact data they need—without having to chain multiple requests together.

---

## Histórico de versão

| Versão | Alteração | Data |
|---|---|---|
|1.0| Construção da página e conteúdo | 28/10/2025 |