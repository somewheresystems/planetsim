# Use an official Node runtime as the base image
FROM node:21-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the frontend code
COPY . .

# Build the app
RUN npm run build

RUN npm install -g webpack webpack-cli

# Expose the port the app runs on
EXPOSE 3000
# Start the app
CMD ["npm", "start"]