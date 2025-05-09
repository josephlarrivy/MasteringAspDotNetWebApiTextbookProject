# Chapter 2 - Understanding HTTP and REST

**REST**: Representational State Transfer

## Software Architecture

**Software Architecture**: a configuration of components, connectors, and data

- Component: An abstract unit of software instructions and the internal state that provides a transformation of data via its interface
- Connector: An abstract mechanism that mediates communication, coordination, or cooperation among components
- Data: An element of information that is transferred from a component, or received by a component, via its connector

## REST Principals

- Applying the following **constraints** to the architecture lets us develop a **RESTful Api**

### Cient - server

- The client-server setup allows the two parts to be developed independently

### Constraint: Stateless

- The server should not containand state of workflow
- The client is the driver of the information that it wants

### Constraint: Cache

- Whenever the server transmits data that will not change, it is refered to as static data
- After data is retreived from the database, it should be cahced as an application layer
- Subsequent requests for the same data can be retreived without another interaction with the database

### Constraint: The uniform interface

- Interfaces exposed by the components are generalized
- The server does not have a knowledge of the consumers

### Constraint: Layered system

- By layering components, we ansure that each component does not know about the layers that its neighbors connect to
- This promotes security by havng boundary walls

### Constraint: Code-on-demand

- Least popular characteristic of REST
- Allows the server to deliver code to the client (book will not cover this any more)

## REST architectural elements

### Data elements

- When a cleint requests a data element from the server, RESTful transfer the data as well as metadata to the client as instructions tocompose the resource

### Resources and resource identifiers

- A resource is any data that needs to be shared
- Resoures should have specific resource identifiers

### Representations

- A representation is a combination of the data you want to share and the metadat associated with it
- The format of the data is the media type

### Connectors

- Types of connectors:
  - client
  - server
  - cache
  - resolver
  - tunnel

- Connectors can be thought of as interfaces
- REST is stateless so every request will have to carry all the information that is requeired for the server to process the request from the client

### Components

- A component in REST architecture would be a web browser on the client and IIS on the server

## HTTP

- After HTTP 1.0, connections with the server are not reused, they are reestablished for each noew request
- A basic HTTP request is composed of a header and a body

### HTTP POST example

- REST POST requests are not idempotent
- This means that when calling the same endpoint more than once, the same behavior should not be expected every time and the same data would be returned
- Given that the cleint is usually sending specific information, the response will be tailored to the POST request and therefore the response will be different for each POST request

### HTTP GET example

- GET is an idempotent meaning that it should return the same data every time
- This ties into the REST principal of statelessness

### HTTP PUT example

- PUT can be used to update a resource
- PUT requests usuaqlly have a body
- The URL for a PUT request usually contains the identifier of the resource being updated
- Behaves similar ot POST requests but are made on reources that already exist
- PUT requests are idempotent

### HTTP DELETE example

- DELETE requests are idempotent
- If the resource exists, a 200 is usually returned
- If the resource does not exist, a 404 is usually returned

## Enhanced Summary of Creating a RESTful API

- Uses nouns for endpoints and follows consistent naming (/users not /getUsers)
- Follows and uses the proper methods correctly (GET, POST, PUT, DELETE)
- Returns the appropriate HTTP status codes (200, 201, 404, etc)
- Is sateless - each requests contains the needed information
- Includes versioning
- Supports pagination, filtering, and sorting via query params
- Secred with HTTPS and proper authentication