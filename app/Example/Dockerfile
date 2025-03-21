# Use .NET SDK to build the project
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /app

# Copy the project to the container working directory
COPY . ./
# Restore the project dependencies
RUN dotnet restore
# Build the project in release mode
RUN dotnet publish -c Release -o out

# Build runtime image
FROM mcr.microsoft.com/dotnet/aspnet:8.0@sha256:6c4df091e4e531bb93bdbfe7e7f0998e7ced344f54426b7e874116a3dc3233ff
WORKDIR /app
COPY --from=build /app/out .
ENTRYPOINT ["dotnet", "Example.dll"]
