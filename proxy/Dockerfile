# Always use stable Alpine images
FROM nginx:stable-alpine

# Remove the default configuration file
RUN rm -rf /etc/nginx/conf.d/default.conf

# Copy the tuned configuration file to the container
COPY nginx.conf /etc/nginx/conf.d

# Copy the certificates for enabling SSL
COPY example.com.br.pem /etc/ssl/example.com.br.pem
COPY example.com.br.key /etc/ssl/example.com.br.key
