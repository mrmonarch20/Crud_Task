
FROM node:14


WORKDIR /usr/src/app


COPY package*.json ./

# Install backend dependencies
RUN npm install

# Copy the rest of the backend code
COPY . .

# Expose the port the backend server runs on
EXPOSE 8080

# Command to run the backend server
CMD ["node", "server.js"]
