# AI Assistant

## Overview

AI Assistant is a Django-based web application designed to assist users with various tasks. This project utilizes Python and Django to provide a robust backend for handling requests and serving content.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Environment Variables](#environment-variables)
- [Managing Migrations](#managing-migrations)
- [Contributing](#contributing)
- [License](#license)

## Features

- User authentication
- Admin panel for managing users and content
- Static file handling
- SQLite database for development
- PostgreSQL database for production

## Installation

To set up the project locally, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/dannybarajas/ai_personalized_assistant.git
   cd ai_assistant
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables:**
   Create a `.env` file in the root directory of the project and add the following variables:
   ```dotenv
   POSTGRES_DB=db_assistant
   POSTGRES_USER=user_assistant
   POSTGRES_PASSWORD=New2025*+
   ```

5. **Run migrations:**
   ```bash
   python manage.py migrate
   ```

## Usage

To start the development server, run:

```bash
docker-compose up --build
```

You can access the application at `http://127.0.0.1:8000/`.

## Configuration

- **Docker:** You can run the application using Docker. The `docker-compose.yml` file is configured to set up both the Django application and a PostgreSQL database.

- **Static Files:** If you need to collect static files, uncomment the relevant line in the `Dockerfile`.

## Environment Variables

The application uses the following environment variables for PostgreSQL configuration:

- `POSTGRES_DB`: The name of the database to create.
- `POSTGRES_USER`: The username for the PostgreSQL superuser.
- `POSTGRES_PASSWORD`: The password for the PostgreSQL superuser.

Make sure to set these variables in the `.env` file as shown in the Installation section.

## Managing Migrations

After starting the application, you can manage your database migrations using the following commands:

1. **Create migrations:**
   ```bash
   docker-compose exec web python manage.py makemigrations
   ```

2. **Apply migrations:**
   ```bash
   docker-compose exec web python manage.py migrate
   ```

3. **Create a superuser:**
   ```bash
   docker-compose exec web python manage.py createsuperuser
   ```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or features.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
