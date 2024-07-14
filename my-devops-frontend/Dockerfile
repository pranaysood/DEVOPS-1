# Use an official Node runtime as a parent image
FROM node:14

# Set the working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json ./
COPY package-lock.json ./
RUN npm install

# Bundle app source inside Docker image
COPY . .

# Build the app
RUN npm run build

# Install serve to serve your app
RUN npm install -g serve

# Command to run your app
CMD ["serve", "-s", "build", "-l", "3000"]
