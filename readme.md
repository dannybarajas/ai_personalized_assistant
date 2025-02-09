# AI Assistant

## Overview

AI Assistant is a Django-based web application designed to assist users with various tasks. This project utilizes Python and Django to provide a robust backend for handling requests and serving content.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## Features

- User authentication
- Admin panel for managing users and content
- Static file handling
- SQLite database for development

## Installation

To set up the project locally, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/dannybarajas/ai_assistant.git
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
   Copy the `.env.example` to `.env` and fill in the necessary values.

5. **Run migrations:**
   ```bash
   python manage.py migrate
   ```

## Usage

To start the development server, run:

```bash
python manage.py runserver
```

You can access the application at `http://127.0.0.1:8000/`.

## Configuration

- **Docker:** You can also run the application using Docker. Build the Docker image and run the container:
  ```bash
  docker build -t ai_assistant .
  docker run -p 8000:8000 ai_assistant
  ```

- **Static Files:** If you need to collect static files, uncomment the relevant line in the `Dockerfile`.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or features.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
