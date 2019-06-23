FROM microsoft/aspnetcore-build AS build-env
#FROM microsoft/aspnetcore:2.0
WORKDIR /app

# Copy everything else and build
COPY . ./

RUN dotnet restore
RUN dotnet build
RUN dotnet publish "./dotnetcore-sample/dotnetcore-sample.csproj" -c Release -o ./out;

#WORKDIR /dotnetcore-sample/out

FROM microsoft/aspnetcore:2.0
WORKDIR /dotnetcoreapp
COPY --from=build-env /app/dotnetcore-sample/out .

EXPOSE 5000

ENTRYPOINT ["dotnet", "dotnetcore-sample.dll"]
