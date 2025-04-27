# Personal Web Project

A full-stack web application built with Go (Gin) backend, NuxtJS frontend, and PostgreSQL database.

personal-web/ ├── backend/ # Go Gin backend │ ├── cmd/ # Main applications of the project │ │ └── api/ # API server entry point │ │ └── main.go │ ├── internal/ # Private application code │ │ ├── config/ # Configuration │ │ ├── handlers/ # HTTP handlers │ │ ├── middleware/ # HTTP middleware │ │ ├── models/ # Database models │ │ ├── repository/ # Database operations │ │ └── services/ # Business logic │ ├── pkg/ # Public libraries that can be used by external applications │ ├── migrations/ # Database migrations │ ├── tests/ # Test files │ ├── .env # Environment variables │ ├── go.mod # Go modules file │ └── go.sum # Go modules checksum │ ├── frontend/ # NuxtJS frontend │ ├── assets/ # Uncompiled assets (fonts, images, etc.) │ ├── components/ # Vue components │ ├── composables/ # Composable functions │ ├── layouts/ # Page layouts │ ├── pages/ # Application views and routes │ ├── plugins/ # Vue plugins │ ├── public/ # Static files │ ├── stores/ # State management (if using Pinia) │ ├── types/ # TypeScript type definitions │ ├── utils/ # Utility functions │ ├── .env # Environment variables │ ├── nuxt.config.ts # Nuxt configuration │ └── package.json # Node dependencies │ ├── docker/ # Docker configuration files │ ├── backend/ # Backend Dockerfile │ ├── frontend/ # Frontend Dockerfile │ └── postgres/ # PostgreSQL initialization scripts │ ├── .gitignore # Git ignore file ├── docker-compose.yml # Docker compose configuration ├── README.md # Project documentation └── Makefile # Build and deployment commands

## Tech Stack

- **Backend**: Go with Gin framework
- **Frontend**: NuxtJS (Vue 3)
- **Database**: PostgreSQL
- **Development**: Docker & Docker Compose

## Project Structure

```
├── backend/         # Go Gin backend
├── frontend/        # NuxtJS frontend
└── docker/          # Docker configuration files
```

## Getting Started

### Prerequisites

- Go 1.21 or later
- Node.js 18 or later
- Docker and Docker Compose
- PostgreSQL

### Development Setup

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd personal-web
   ```

2. Start the development environment:
   ```bash
   docker-compose up -d
   ```

3. Backend development:
   ```bash
   cd backend
   go mod download
   go run cmd/api/main.go
   ```

4. Frontend development:
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

## License

[Your chosen license]
