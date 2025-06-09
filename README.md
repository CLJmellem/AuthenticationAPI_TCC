# AuthenticationAPI_TCC

## Overview
AuthenticationAPI_TCC is a .NET 9.0-based project designed to provide authentication and authorization services. It leverages ASP.NET Core Identity for user management and role-based access control. The project is configured to use SQL Server as its database provider for storing user credentials and related data.

## Features
- User authentication and authorization using ASP.NET Core Identity.
- Role-based access control.
- Integration with SQL Server for data persistence.
- Swagger support for API documentation and testing.

## Prerequisites
- [.NET 9.0 SDK](https://dotnet.microsoft.com/download/dotnet/9.0)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
- A code editor like [Visual Studio Code](https://code.visualstudio.com/) or Visual Studio.

## Setup Instructions

1. Configure the database connection:
    -Open the `appsettings.json` file located in `src/Services/Authentication/Authentication.api/`.
    - Update the `DefaultConnection` string under `ConnectionStrings` with your SQL Server details.Configure the database connection:
    ```
    "ConnectionStrings":{
          "DefaultConnection": "Server=localhost,1433;Database=AuthenticatonAPI_TCC;User Id=<your-username>;Password=<your-password>;Encrypt=False;"
        }
    ```

2. Apply database migrations:
```
cd src/Services/Authentication/Authentication.api
dotnet ef database update
```

3. Run the application:
```dotnet run```


## Project Structure
- **Authentication.api**: The main API project for authentication services.
- **Authentication.Core**: Core building blocks for shared functionality.
- **Authentication.WebApp.MVC**: A web application for managing authentication-related tasks.


## Notes
- Ensure that SQL Server is running and accessible before starting the application.
- Use the Development environment for local debugging, as configured in launchSettings.json.

## License
This project is licensed under the MIT License.
