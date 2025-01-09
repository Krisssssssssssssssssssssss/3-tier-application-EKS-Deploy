FROM mcr.microsoft.com/dotnet/aspnet:7.0 AS base
WORKDIR /app
EXPOSE 80

FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
WORKDIR /src

# Copy all files
COPY . .

# Build the application
WORKDIR "/src/Basic3TierAPI"
RUN dotnet build -c Release -o /app/build

FROM build AS publish
RUN dotnet publish -c Release -o /app/publish /p:UseAppHost=false

# Use the runtime image
FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .

# Start the backend application
ENTRYPOINT ["dotnet", "Basic3TierAPI.dll"]
