# Use Node.js base image
FROM node:14

# Set working directory inside container
WORKDIR /app

# Copy dependency files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy your backend code
COPY . .

# Expose the backend port
EXPOSE 3000

# Start the server
CMD ["npm", "start"]
