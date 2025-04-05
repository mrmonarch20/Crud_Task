# Use the official Node.js 14 image as the base image
FROM node:14

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install backend dependencies
RUN npm install

# Copy the rest of the backend application code
COPY . .

# Expose the port the backend server runs on
EXPOSE 8080

# Command to run the backend server
CMD ["node", "server.js"]
