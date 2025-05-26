 This project demonstrates building, and deploying simple .NET web apps using Docker containers.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- [.NET 6.0 SDK](https://dotnet.microsoft.com/download)
- [Docker Desktop](https://www.docker.com/products/docker-desktop) (or equivalent Docker engine)
- Git (for version control)
- IDE/Editor (Visual Studio, VS Code, Rider, etc.)

## Getting Started

### Local Development (Without Docker)

1. Clone the repository
   git clone https://github.com/yourusername/SimpleWebApp.git
   cd SimpleWebApp
   
2. Restore dependencies

   dotnet restore
   

4. Run the application

    dotnet run
   
6. Open http://localhost:5000 in your browser to access ur application

### Docker Development

#### Build the Docker Image

docker build -t simplewebapp .


#### Run the Container

docker run -d -p 5000:80 --name webapp simplewebapp

Open http://localhost:5000 to view the running application.

#### Stop the Container

docker stop webapp


## Deployment

### Push to Docker Registry

1. Tag your image (replace yourusername with your Docker Hub username)

   docker tag simplewebapp yourusername/simplewebapp:latest
   
2. Push to Docker Hub
    docker push yourusername/simplewebapp:latest
