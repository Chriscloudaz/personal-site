# Use the official Nginx image from the Docker Hub
FROM nginx:alpine

# Copy the static HTML files and directories to the Nginx HTML directory
COPY index.html /usr/share/nginx/html/
COPY css /usr/share/nginx/html/css/
COPY img /usr/share/nginx/html/img/
COPY js /usr/share/nginx/html/js/
COPY fonts /usr/share/nginx/html/fonts/
COPY scss /usr/share/nginx/html/scss/

# Expose port 80
EXPOSE 80

# Start Nginx when the container launches
CMD ["nginx", "-g", "daemon off;"]