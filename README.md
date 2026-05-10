# Movies API

A **RESTful ASP.NET Core Web API** for managing a movies catalog with genres — featuring image upload support, AutoMapper, and EF Core persistence.

## What it does

Provides API endpoints to manage a movie database. Each movie belongs to a genre, has metadata (title, year, rate, storyline), and can have a poster image. The API uses a service layer pattern to keep controllers clean.

## Tech Stack

- **ASP.NET Core Web API** (.NET)
- **Entity Framework Core** — Code-First with SQL Server
- **AutoMapper** — entity ↔ DTO mapping
- **Swagger / OpenAPI**

## Key Features

- Genre management (CRUD)
- Movie management with genre association
- Image upload and storage for movie posters
- DTO pattern for create, read, and detail views
- Service layer (`IGenresService`, `IMoviesService`) separating business logic from controllers

## API Endpoints

| Method | Route | Description |
|---|---|---|
| GET | `/api/genres` | List all genres |
| POST | `/api/genres` | Create a genre |
| GET | `/api/movies` | List all movies |
| POST | `/api/movies` | Create a movie with poster |
| GET | `/api/movies/{id}` | Get movie details |
| PUT | `/api/movies/{id}` | Update a movie |
| DELETE | `/api/movies/{id}` | Delete a movie |

## Getting Started

1. Set your SQL Server connection string in `appsettings.json`.
2. Apply migrations: `dotnet ef database update`
3. Run: `dotnet run --project MoviesAPI`
