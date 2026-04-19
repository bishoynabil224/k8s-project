# Use official NGINX lightweight image
FROM nginx:alpine

# Remove default NGINX config
RUN rm /etc/nginx/conf.d/default.conf

# Copy your custom NGINX config
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy static frontend files
COPY index.html /usr/share/nginx/html/index.html


EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]