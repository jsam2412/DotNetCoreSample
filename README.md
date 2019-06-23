# Sample ASP.NET Core application for Docker Container docs
# test

For information on how to use this repository, see [.NET Core](https://docs.microsoft.com/azure/devops/pipelines/languages/dotnet-core).

Commands to Build Docker Image and Run Container in EC2 Linux Instance


Step 1:
Pull latest from Git on EC2


Step 2: Build docker image:

Go to src folder and run below commands

docker build dotnetcoreapp .

docker images


Step 3: Run below command to run docker container:

docker run -d -p 80:80 dotnetcoreapp

docker container ls


Step 4: Open HTTP port 80 for your EC2 instance in AWS (open port in inbound traffic).


Step 5: Access application in browser using Public DNS (IPv4).



