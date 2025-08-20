# Chat App

This is a Django-based chat application with user authentication and real-time messaging using Django Channels.

## Features

- User registration and login
- Real-time chat functionality
- Group and private messaging
- Responsive UI with templates

## Prerequisites

- Python 3.10+
- pip
- SQLite (default, no setup required)

## Installation

1. **Clone the repository:**
   ```bash
   git clone <repo-url>
   cd chat_app
   ```
2. **Create a virtual environment (recommended):**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## Database Setup

1. **Apply migrations:**
   ```bash
   python manage.py migrate
   ```
2. **Create a superuser (optional, for admin access):**
   ```bash
   python manage.py createsuperuser
   ```

## Running the Application

1. **Start the development server:**
   ```bash
   python manage.py runserver
   ```
2. **Access the app:**
   Open your browser and go to `http://127.0.0.1:8000/`

## WebSocket/Channels Setup

- The app uses Django Channels for real-time chat. For local development, the default ASGI setup is sufficient.
- For production, configure a channel layer (e.g., Redis) in `chat_app/settings.py`.

## Folder Structure

- `chat/` - Chat logic, consumers, models, routing
- `users/` - User authentication and profile management
- `templates/` - HTML templates
- `chat_app/` - Project settings and configuration

## Running Tests

```bash
python manage.py test
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

MIT
