# Task Monitor API

## Overview
Task Monitor is a RESTful API built with .NET Web API and MongoDB for managing and tracking tasks efficiently. This API allows users to create, update, delete, and retrieve tasks in a structured manner.

## Features
- Create new tasks
- Retrieve all tasks or a specific task
- Update task details
- Delete tasks
- Mark tasks as completed or pending

## Technologies Used
- .NET Web API
- MongoDB
- C#
- ASP.NET Core
- MongoDB Driver for .NET

## Prerequisites
Ensure you have the following installed:
- .NET SDK (Latest version)
- MongoDB (Locally or via cloud service like MongoDB Atlas)
- Postman (Optional, for API testing)

## Installation & Setup
### Clone the Repository
```sh
git clone https://github.com/yourusername/task-monitor.git
cd task-monitor
```
### Configure MongoDB Connection
Update `appsettings.json` with your MongoDB connection string:
```json
"MongoDB": {
  "ConnectionString": "mongodb://localhost:27017",
  "DatabaseName": "TaskMonitorDB",
  "TaskCollection": "Tasks"
}
```

### Build and Run the Project
```sh
dotnet restore
dotnet build
dotnet run
```

## API Endpoints
### Task Management
#### Create a Task
**POST** `/api/tasks`
```json
{
  "title": "Complete project documentation",
  "description": "Write the README file for Task Monitor API",
  "status": "Pending"
}
```

#### Get All Tasks
**GET** `/api/tasks`

#### Get a Task by ID
**GET** `/api/tasks/{id}`

#### Update a Task
**PUT** `/api/tasks/{id}`
```json
{
  "title": "Update API Documentation",
  "description": "Modify the README file",
  "status": "Completed"
}
```

#### Delete a Task
**DELETE** `/api/tasks/{id}`

## Error Handling
- Returns `400 Bad Request` for invalid input.
- Returns `404 Not Found` if the task ID does not exist.
- Returns `500 Internal Server Error` for unexpected server errors.

## Future Enhancements
- Implement authentication and authorization
- Add filtering and sorting options
- Enable task reminders and notifications

## License
This project is licensed under the MIT License.

## Author
Ahmeed Abdul-Jalal

---
Happy coding! 🚀

Email : ahmeedabduljalal@gmail.com
