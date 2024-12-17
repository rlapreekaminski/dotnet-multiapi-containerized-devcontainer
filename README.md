# 🚀 .NET Multi-API Project with Dev Containers

This project contains two minimal APIs developed using **ASP.NET Core**. It is configured for local development using **Dev Containers** and Docker Compose.

## 📁 Project Structure

The project structure is as follows:

```plaintext
dotnet-multiapi-containerized-devcontainer/
├── .devcontainer/            # Dev Container configuration
│   ├── devcontainer.json
│   └── Dockerfile            # Development environment configuration
├── .vscode/                  # VS Code configuration
│   ├── tasks.json
│   └── launch.json
├── src/
│   ├── api1/                 # Source code for the first API
│   │   ├── api1.csproj
│   │   ├── Program.cs
│   │   └── ...
│   ├── api2/                 # Source code for the second API
│   │   ├── api2.csproj
│   │   ├── Program.cs
│   │   └── ...
├── docker/                   # Dockerfiles for each API
│   ├── Dockerfile.api1       # Dockerfile for API1
│   ├── Dockerfile.api2       # Dockerfile for API2
├── docker-compose.yml        # Docker Compose for running both APIs
└── README.md                 # Documentation (you are here)
```

## ⚙️ Prerequisites

Before starting, ensure you have the following tools installed:

- **[Docker Desktop](https://www.docker.com/products/docker-desktop/)** (to run containers locally)
- **[Visual Studio Code](https://code.visualstudio.com/)** with the **Dev Containers** extension (`ms-vscode-remote.remote-containers`)
- **[.NET SDK 9.0](https://dotnet.microsoft.com/download)** only if you or a member of your team want to work outside the container

## 🚧 Getting Started

### 1. Launch Development Environment with Dev Containers

Open the project in VS Code.

Ensure the Dev Containers extension is installed.

Open the command palette (Ctrl+Shift+P or Cmd+Shift+P) and select:

```bash
Dev Containers: Reopen in Container
```

This will rebuild and launch the development environment inside a Docker container.

### 2. Build and Run the APIs with Docker Compose

To run both APIs simultaneously in Docker containers, use the following command:

```bash
docker-compose up --build
```

The APIs will be accessible at the following addresses:

- API1: <http://localhost:5136>
- API2: <http://localhost:5137>

### 3. Debugging with VS Code

To debug an API:

- Place breakpoints in your code.
- Use the pre-configured **_launch.json_** file to debug either API1 or API2.
- Start debugging with F5.+

## 🔗 Useful Resources

- [.NET Minimal API Documentation](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/minimal-apis/overview?view=aspnetcore-9.0)
- [Docker Compose Documentation](https://docs.docker.com/compose/)
- [Dev Containers based on Dockefile Documentation](https://code.visualstudio.com/docs/devcontainers/create-dev-container#_dockerfile)

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)
