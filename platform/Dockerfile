# Use Node.js as base image
FROM node:14

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the files
COPY . .

# Build the app

RUN npm run build

# Install http-server to serve the app
RUN npm install -g http-server

# Command to run the app

CMD [ "http-server", "build", "-p", "3000" ]