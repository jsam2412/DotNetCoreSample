#FROM microsoft/aspnetcore-build:1.1.2 AS build-env
FROM microsoft/aspnetcore:2.0
WORKDIR /app

# Copy everything else and build
COPY . ./

RUN dotnet restore
RUN dotnet build
RUN dotnet publish "./dotnetcore-sample/dotnetcore-sample.csproj" -c Release -o ./out;

WORKDIR /dotnetcore-sample/out

ENTRYPOINT ["dotnet", "dotnetcore-sample.dll"]
