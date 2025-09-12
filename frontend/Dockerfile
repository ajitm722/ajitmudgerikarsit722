# frontend/Dockerfile
FROM nginx:alpine

# Copy our Nginx site config
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy static assets (index.html, main.js, etc.)
COPY . /usr/share/nginx/html

EXPOSE 80

# Nginx is the entrypoint; nothing else needed
