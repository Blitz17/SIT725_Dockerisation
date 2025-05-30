# Use official Node.js image
FROM node:18-alpine

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install all dependencies, including dotenv
RUN npm install

# Copy the entire backend code into the container
COPY . .

# Expose the backend port (adjust if needed)
EXPOSE 3000

# Run the backend
CMD ["node", "server.js"]