# Backend dockerfile for PRODUCTION
# Created @ Ago, 4th, 2022 by Herick Vinicius

# Always use LTS-ALPINE images
FROM node:lts-alpine

# Create /app folder at /usr/src directory
RUN mkdir -p /usr/src/app
# Set your /app directory as the current workdir
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# IMPORTANT: Update NPM before installing any packages
RUN npm install --location=global npm@latest
# Install packages
RUN npm install

# Copy all source files inside the container
COPY . .

# Expose some port so the app can be seen by the proxy
EXPOSE 2000

# Serve it!
CMD [ "npm", "start" ]