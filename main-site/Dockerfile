# Use the official Nginx image from the Docker Hub
FROM nginx:alpine

# Copy the static HTML files to the Nginx HTML directory
COPY index.html /usr/share/nginx/html
COPY /css /usr/share/nginx/html/css/
COPY /favicon_io /usr/share/nginx/html/favicon_io

# Expose port 80 to the outside world
EXPOSE 80

# Start Nginx when the container launches
CMD ["nginx", "-g", "daemon off;"]