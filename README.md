# Sample ASP.NET Core application for Azure Pipelines docs
# test

For information on how to use this repository, see [.NET Core](https://docs.microsoft.com/azure/devops/pipelines/languages/dotnet-core).

Commands to Build Docker Image and Run Container in EC2 Linux Instance

Step 1:
Pull latest from Git on EC2

Step 2: Build container commands:
docker build dotnetcore .
docker images

Step 3: Run container commands:
docker run -d -p 80:80 dotnetcoreapp
docker container ls


