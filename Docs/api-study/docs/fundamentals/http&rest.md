# HTTP e REST 

[Fonte 1](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods) e [Fonte 2](https://restfulapi.net/) deste conteúdo. 

---

## HTTP request methods

HTTP defines a set of **request methods** to indicate the purpose of the request and what is expected if the request is successful. Here comes some of the most important methods of the protocol:

### GET

The GET method requests a representation of the specified resource. Requests using GET should only retrieve data and should not contain a request content.

### POST

The POST method submits an entity to the specified resource, often causing a change in state or side effects on the server.

### PUT 

The PUT method replaces all current representations of the target resource with the request content.

### DELETE

The DELETE method deletes the specified resource.

---
Now, follow other existing methods of the protocol that can be used:

### HEAD

The HEAD method asks for a response identical to a GET request, but without a response body.

### CONNECT

The CONNECT method establishes a tunnel to the server identified by the target resource.

### OPTIONS

The OPTIONS method describes the communication options for the target resource.

### TRACE

The TRACE method performs a message loop-back test along the path to the target resource.

### PATCH

The PATCH method applies partial modifications to a resource.

---

## What is REST?

REST is an acronym for REpresentational State Transfer and an architectural style for distributed hypermedia systems. REST is not a protocol or a standard, it is an architectural style. During the development phase, API developers can implement REST in a variety of ways.

Like the other architectural styles, REST also has its guiding principles and constraints. These principles must be satisfied if a service interface is to be referred to as RESTful.

### The Six Guiding Principles of REST

#### Uniform Interface

The following four constraints can achieve a uniform REST interface:

- **Identification of resources** – The interface must uniquely identify each resource involved in the interaction between the client and the server.

- **Manipulation of resources through representations** – The resources should have uniform representations in the server response.

- **Self-descriptive messages** – Each resource representation should carry enough information to describe how to process the message. It should also provide information on the additional actions that the client can perform on the resource.

- **Hypermedia as the engine of application state** – The client should have only the initial URI of the application. The client application should dynamically drive all other resources and interactions with the use of hyperlinks.

In simpler words, REST defines a consistent and uniform interface for interactions between clients and servers.

### Client-Server

The client-server design pattern enforces the separation of concerns, which helps the client and the server components evolve independently.

By separating the user interface concerns (client) from the data storage concerns (server), we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components.

While the client and the server evolve, we have to make sure that the interface/contract between the client and the server does not break.

### Stateless

Statelessness mandates that each request from the client to the server must contain all of the information necessary to understand and complete the request.

### Cacheable

The cacheable constraint requires that a response should implicitly or explicitly label itself as cacheable or non-cacheable.

###  Layered System

The layered system style allows an architecture to be composed of hierarchical layers by constraining component behavior. In a layered system, each component cannot see beyond the immediate layer they are interacting with.

A layman’s example of a layered system is the MVC pattern. The MVC pattern allows for a clear separation of concerns, making it easier to develop, maintain, and scale the application.

### Code on Demand (Optional)

REST also allows client functionality to be extended by downloading and executing code in the form of applets or scripts.

---

## What is a resource?

The key abstraction of information in REST is a resource. Any information that we can name can be a resource.

The state of the resource at any particular time is known as the resource representation. The resource representations consist of:

- the data;
- the metadata describing the data;
- and the hypermedia links that can help the clients transition to the next desired state.

### Resource Identifiers

REST uses resource identifiers to identify each resource involved in the interactions between the client and the server components

#### Hypermedia

The data format of a representation is known as a media type. The media type identifies a specification that defines how a representation is to be processed. A RESTful API looks like **hypertext**. 

#### Self-Descriptive

Resource representations shall be self-descriptive: the client does not need to know if a resource is an employee or a device. It should act based on the media type associated with the resource.

---

## Example

```JSON
{
  "id": 123,
  "title": "What is REST",
  "content": "REST is an architectural style for building web services...",
  "published_at": "2023-11-04T14:30:00Z",
  "author": {
    "id": 456,
    "name": "John Doe",
    "profile_url": "https://example.com/authors/456"
  },
  "comments": {
    "count": 5,
    "comments_url": "https://example.com/posts/123/comments"
  },
  "self": {
    "link": "https://example.com/posts/123"
  }
}
```

---

## Histórico de versão

| Versão | Alteração | Data |
|---|---|---|
|1.1| Construção da página e conteúdo | 28/10/2025 |