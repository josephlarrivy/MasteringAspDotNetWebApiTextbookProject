# Chapter 3 - Anatomy of ASP.NET Core Web API

## A quick recap of the MVC framework

- ASP.NET Core Web APIs are simmilar to MVC
- They use Models, Controllers, and the View is the data that is returned by the response
- ASP.NET MVC:
  - Models: classes that represent the domain model and the data stored in the database
  - Views: dynamically generated HTML pages
  - Controllers: classes that manage the interaction between the view and the model

### Introducing web API

- **Web API**: any methods that are accessable over the web
- Successful APIs have infrastructure like hosting, chacheing, concurrency, logging, security, etc
- An ASP.NET Web API lives on the ASP.NET Framework
- ASP.NET has become more powerful over the years by implementing async/await, LINQ, Entity Framework, Dependency Injection, etc

### ASP.NET into Open Source world

| Framework        | Open-source   | Cross-platform |
|------------------|---------------|----------------|
| .NET Framework   | No            | No             |
| .NET Core        | Yes           | Yes            |
| ASP.NET Core     | Yes           | Yes            |


### Introduction to .NET Core

- .NET Core can be developed, tested, and deployed on Windows, Linux, and Mac
- .NET Core contains a subset of the original .NET Framework but come with its own set of APIs
- ASP.NET Core application can work on the existing .NET Framewrok but not vice versa
- .NET Core points:
  - Can be installed cross-platform
  - Modular - NuGet packages can be installed
  - .NET Core can be self-hosted and run as a stand-along app
- .NET Core CLI commands:
  - new: Initializes a basic .NET project
  - restore: Restores dependencies specified in the .NET project (usually runs automatically)
  - build: Builds a .NET project
	- Performs a routine build and generates the bin and obj folders
  - publish: Publishes a .NET project for deployment (including the runtime)
	- Will create the publish folder under the bin directory - this folder can be ported to any machine that has the .Net Core SDK installed
  - run: Compiles and immediately executes a .NET project
  - test: Runs unit tests using the test runner specified in the project
  - pack: Creates a NuGet package

### Introducing ASP.NET CORE

- ASP.NET Core is and open-source cross-platform framework for building modern, cloud-based web applications using .NET

### An overview of ASP.NET Core

- ASP.NET Core runs both Full .NET Framework and .NET Core
- ASP.NET Core application with .NET Framework can only be developed and deployed on Windows machines
- ASP.NET Core Developers can work on and machine, not confined to Visual Studio IDE
- ASP.NET Core can run with different versions of .NET Core

In addition to being cross-platform, ASP.NET Core has additional advantages:

- Modular approach to NuGet packages - only need the ones you need (keeps code lightweight)
- Has seamless integration with modern web frameworks like Angular, Node, Bootstrap
- Has built-in Dependency Injection
- Can be hosted on IIS or self-hosted

### ASP.NET Core Web API Application structure


| File/folder      | Purpose   |
|------------------|-----------|
| /Controllers     | contains controller classes that handle requests   |
| Program.cs       | entry point for the application execution   |
| Startup.cs       | Sets up the configuration and wires up the services that the application will use   |
| AppSettings.json | key/value based configurations setting file   |
| Web.config       | strictly used for IIS configuration, invokes the app when running on IIS   |

## Program.cs

