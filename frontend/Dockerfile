# Stage 1: Build Angular App
FROM node:14 as builder

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build --prod

# Stage 2: Serve with http-server
FROM node:14-alpine

RUN npm install -g http-server

WORKDIR /app

# Copy the correct Angular build output
COPY --from=builder /app/dist/angular-15-crud /app

EXPOSE 8081

CMD ["http-server", "/app", "-p", "8081"]
