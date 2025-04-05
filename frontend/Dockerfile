# Use  Node.js 14 image as the base image
FROM node:14

# Set the working directory
WORKDIR /usr/src/app

# Copy dependency definitions
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy source files
COPY . .

# Build the Angular application
RUN npm run build --prod

# Install http-server to serve the built files
RUN npm install -g http-server

# Expose the frontend port
EXPOSE 8081

# Start the app
CMD ["http-server", "dist/frontend", "-p", "8081"]
