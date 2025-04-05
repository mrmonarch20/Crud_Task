# Use Node.js base image
FROM node:14

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy the entire source code
COPY . .

# Build the Angular app (production mode)
RUN npm run build --prod

# Install http-server to serve the built app
RUN npm install -g http-server

# Set working directory to the Angular build output
WORKDIR /app/dist/angular-15-crud

# Expose the port the app runs on
EXPOSE 8081

# Start the server
CMD ["http-server", "-p", "8081"]

