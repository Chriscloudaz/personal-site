# Use the official Nginx image from the Docker Hub
FROM nginx:alpine

# Copy the static HTML files and directories to the Nginx HTML directory
COPY site-content/. /usr/share/nginx/html/

# Expose port 80
EXPOSE 80

# Start Nginx when the container launches
CMD ["nginx", "-g", "daemon off;"]