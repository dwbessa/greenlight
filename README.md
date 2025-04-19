# Greenlight

Greenlight is a REST API for movies built with Go, following the "Let's Go Further" book by Alex Edwards.

## Project Overview

Greenlight is a RESTful API that allows clients to create, read, update, and delete information about movies. It's built using modern Go practices and follows a clean architecture approach.

## Features (in progress)

- RESTful API endpoints for movie management
- JSON response formatting
- Custom data validation
- Structured error handling
- PostgreSQL database integration (coming soon)
- Authentication and authorization (coming soon)

## Project Structure

```
greenlight/
├── bin/           # Compiled application binaries
├── cmd/           # Application-specific code
│   └── api/       # API application
├── internal/      # Private application code
│   └── data/      # Data access layer
├── migrations/    # SQL migrations
└── remote/        # Configuration for deployment
```

## API Endpoints

| Method | URL Pattern       | Handler            | Action                     |
|--------|-------------------|--------------------|-----------------------------|
| GET    | /v1/healthcheck   | healthcheckHandler | Show application information|
| POST   | /v1/movies        | createMovieHandler | Create a new movie          |
| GET    | /v1/movies/:id    | showMovieHandler   | Show details of a movie     |

## Getting Started

### Prerequisites

- Go 1.24 or higher

### Running the API

```bash
# Run the API with default settings (port 4000)
go run ./cmd/api

# Run on a different port
go run ./cmd/api -port=5000

# Run in a specific environment
go run ./cmd/api -env=production
```

## Current Progress

- [x] Basic API structure
- [x] JSON response handling
- [x] Router configuration
- [x] Custom data types (Runtime)
- [ ] Data validation
- [ ] Database integration
- [ ] Authentication

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

This project is based on the "Let's Go Further" book by Alex Edwards.