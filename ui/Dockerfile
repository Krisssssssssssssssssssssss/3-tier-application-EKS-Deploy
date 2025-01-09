# Use an official Nginx runtime as the base image
FROM nginx:alpine

# Set the working directory
WORKDIR /usr/share/nginx/html

# Copy all frontend files to the default Nginx web root
COPY . .

# Copy the configuration file for dynamic API URLs
COPY config/config.json ./config/config.json

# Expose port 80
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]
