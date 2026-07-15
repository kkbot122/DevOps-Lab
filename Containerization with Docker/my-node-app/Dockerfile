# Use the Node.js 18-alpine base image (alpine is a lightweight Linux
FROM node:18-alpine
# Set the working directory inside the container
WORKDIR /app
# Copy the package.json and package-lock.json files
# We copy these first to leverage Docker's layer caching
COPY package*.json ./
# Install the Node.js dependencies
RUN npm install
# Copy the application code into the working directory
COPY . .
# Expose the port the application listens on
EXPOSE 3000
# Define the command to run the application
CMD ["node", "server.js"]