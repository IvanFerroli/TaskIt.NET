# Use the official .NET SDK as the base image
FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

# Use the .NET SDK for building the application
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src
COPY ["TaskManager.csproj", "./"]
RUN dotnet restore "./TaskManager.csproj"
COPY . .
RUN dotnet build "TaskManager.csproj" -c Release -o /app/build

# Final runtime image
FROM build AS publish
RUN dotnet publish "TaskManager.csproj" -c Release -o /app/publish

# Use the final runtime image
FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "TaskManager.dll"]
