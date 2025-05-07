
Chapter 1 - Introduction to Microservices and Service-Oriented Architecture (SOA)


Services in SOA
	Service: a piece of software that provides functionality to other pieces of software within an application
	- SOA was successful because:
		- It allows for the scaling of software. Additional instances of the service can be created and the request load can be directed to other instances
		- SOA boasts having standardized contracts or interfaces. Services can be upgraded or changed but keep the same call from the client. The service can be upgraded without updating the client
		- Services are stateless. When a series of calls come in to the server, the server doesn't need to remeber the previous calls

Service implementation
	- SOA gained popularity because it operates over standardized internet protocals that are independent of OS platforms or programming languages
	- Can be used to build a RESTful HTTP api
	- Can be used to wrap a legacy system to make the system a REST api

Monolithic architecture
	- Work in a way that is opposite of what SOA tries to achieve
	- Often have an entier website packaged into a single package
	- One package contains everything and that package grows as the website grows
	- Other drawbacks of monolithic architecture
		- The entire ststem needs to be re-deployed even for minor bug fixes
		- One large codebase means sticking with one technology stack
		- Hard to adopt new technologies due to being locked into one big stack
		- Cannot scale up certain functionality that is more in demand without scaling up all of the stack

Introducing microservices
	- Microservices - small, autonomous services that perform one function well
	- Advantage: Lightweight yet scalable
		- A microservice with a group of related functions can be scaled up to handle a larger load without having to scale the entire application's code
	- Advantage: Technology agnostic
		- Use an open communication protocol so that many clients can comunicate with the service
		- Easy to communicate with HTTP REST JSON-based calls
	- Advantage: Independently changeable
		- can upgrade, enhance, fix a specific service without changing the client or the other services in the codebase

