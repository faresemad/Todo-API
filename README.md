# Todo-API

## Todo-API is a simple RESTful API built with Django that allows users to create, retrieve, update, and delete tasks.

## Getting Started

 To get started, follow these steps:

 1. Clone the repository: `git clone https://github.com/faresemad/Todo-API.git`
2. Install the requirements: `pip install -r requirements.txt`
3. Run the migrations: `python manage.py migrate`
4. Create a superuser: `python manage.py createsuperuser`
5. Start the server: `python manage.py runserver`

You can then access the API at `http://localhost:8000/api/tasks/`. 

## API Endpoints

The API has the following endpoints:

- `GET /api/tasks/`: Retrieve a list of all tasks.
- `POST /api/tasks/`: Create a new task.
- `GET /api/tasks/{id}/`: Retrieve a specific task by ID.
- `PUT /api/tasks/{id}/`: Update a specific task by ID.
- `DELETE /api/tasks/{id}/`: Delete a specific task by ID.

## Authentication

All endpoints require authentication except for `POST /api/tasks/`. You can authenticate by sending an HTTP `Authorization` header with a token obtained from the `/api/token/` endpoint. 

To obtain a token, send a `POST` request to `/api/token/` with your `username` and `password` in the request body. The response will contain a token which you can then use in subsequent requests.

## Rate Limiting

The API has rate limiting implemented using Django Ratelimit. By default, each user is limited to 100 requests per day.

## Contributing

If you'd like to contribute to Todo-API, please follow these steps:

1. Fork the repository
2. Create a new branch: `git checkout -b my-new-branch`
3. Make your changes and commit them: `git commit -m "Add some feature"`
4. Push to the branch: `git push origin my-new-branch`
5. Create a pull request

## License

Todo-API is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
