# chat project

# Python Chat Application

This is a real-time chat application built with Python and Django. It uses Django Channels to handle WebSockets and Channels Redis for channel layer backends. The application also uses Daphne as an HTTP and WebSocket protocol server. Celery is used for background tasks, with RabbitMQ serving as the message broker.

## Installation

Before running the application, you need to install the necessary Python packages and RabbitMQ. You can do this using the following commands:

```bash
pip install django daphne channels channels_redis celery
```

```bash
sudo apt-get install rabbitmq-server
```


## Running the Application

1. **Start RabbitMQ Server:**
    ```bash
    sudo service rabbitmq-server start
    ```

2. **Run Celery Worker:**
    In a separate terminal:
    ```bash
    celery -A chatproject worker --loglevel=info
    ```

3. **Run Django Development Server:**
    ```bash
    python manage.py runserver
    ```


## Installation

1. Clone the repository: `git clone https://github.com/yourusername/chatproject.git`
2. Navigate to the project directory: `cd chatproject`
3. Install the requirements: `pip install -r requirements.txt`
4. Run the migrations: `python manage.py migrate`
5. Start the server: `python manage.py runserver`
   
After following these steps, your application should be up and running. You can access it in your web browser at `http://localhost:8000`.

