# Use the official Nginx image from the Docker Hub
FROM nginx:alpine

# Copy the static HTML files and directories to the Nginx HTML directory
COPY resume-site/index.html /usr/share/nginx/html/
COPY resume-site/css /usr/share/nginx/html/css/
COPY resume-site/img /usr/share/nginx/html/img/
COPY resume-site/js /usr/share/nginx/html/js/
COPY resume-site/fonts /usr/share/nginx/html/fonts/
COPY resume-site/scss /usr/share/nginx/html/scss/

# Expose port 80
EXPOSE 80

# Start Nginx when the container launches
CMD ["nginx", "-g", "daemon off;"]