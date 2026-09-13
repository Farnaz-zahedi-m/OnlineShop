# OnlineShop

An e-commerce web application built with **ASP.NET Core 9 MVC**, **Entity Framework Core 9**, **SQL Server**, and **Clean Architecture**.

## Technologies

* ASP.NET Core 9 MVC
* C#
* Entity Framework Core 9
* SQL Server
* Clean Architecture
* Repository Pattern
* Service Layer
* AutoMapper
* ASP.NET Core Identity PasswordHasher
* Bootstrap
* JavaScript / jQuery
* HTML / CSS
* Docker
* Docker Compose
* Git & GitHub

## Features

* User registration and login
* Password hashing
* User management
* Role management
* Role-based authorization
* Admin area
* Product group management
* Product management
* Product image and gallery management
* Product filtering by group
* Product details
* Shopping cart
* Add and remove products from cart
* Product pagination
* Responsive UI with Bootstrap
* Dockerized application environment
* Docker Compose configuration

## Architecture

The project follows a **Clean Architecture** structure with clear separation of concerns:

```text
OnlineShop
│
├── Web
├── Application
├── Domain
├── Infrastructure.Data
└── Infrastructure.IoC
```

### Layers

* **Web Layer** — MVC controllers, views, authentication, and presentation logic
* **Application Layer** — application services, DTOs, interfaces, and business operations
* **Domain Layer** — entities and core domain logic
* **Infrastructure Data Layer** — Entity Framework Core, DbContext, repositories, and database access
* **Infrastructure IoC Layer** — dependency injection and service registration

## Docker

The application can be built and run using Docker and Docker Compose.

### Run with Docker Compose

Make sure **Docker Desktop** is installed and running.

Clone the repository:

```bash
git clone https://github.com/Farnaz-zahedi-m/OnlineShop.git
cd OnlineShop
```

Build and start the application:

```bash
docker compose up --build
```

To run the containers in the background:

```bash
docker compose up -d
```

To stop the application:

```bash
docker compose down
```

## Project Status

**In Development**

The project is actively being developed. Additional backend and API functionality is planned as part of the next development stage.

## Developer

**Farnaz Zahedi Moghadam**
Software Engineer | .NET Developer
