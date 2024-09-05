# Use the official image as a parent image
# Description: Dockerfile for the client side of the MERN stack application

# Use the official image as a parent image
FROM node:18.9.1

# Set the working directory
WORKDIR /app

# Copy the file from your host to your current location
COPY package.json .

# Run the command inside your image filesystem
RUN npm install

# Inform Docker that the container is listening on the specified port at runtime
EXPOSE 5173

# Copy the rest of your app's source code from your host to your image filesystem
COPY . .

# Run the specified command within the container
CMD ["npm", "run", "dev"]


# ----------------------------------------------------------
# # Stage 1: Build Stage
# FROM node:18.9.1 AS build

# # Set the working directory for the build stage
# WORKDIR /app

# # Copy package.json and package-lock.json (if present) to the working directory
# COPY package*.json .

# # Install dependencies defined in package.json
# RUN npm install

# # Copy the rest of the application code to the working directory
# COPY . .

# # Stage 2: Production Stage
# FROM node:18-alpine

# # Set the working directory for the production stage
# WORKDIR /app

# # Copy the built application code from the build stage to the production stage
# COPY --from=build /app /app

# # Expose port 5173 to allow external access
# EXPOSE 5173

# # Command to run the application in development mode
# CMD ["npm", "run", "dev"]
