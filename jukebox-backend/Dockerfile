# Use Node.js base image
FROM node:18-alpine

# Set working directory inside container
WORKDIR /app

# Install Node dependencies
COPY package*.json ./
RUN npm install

# Copy React app source
COPY . .

# Expose React port
EXPOSE 3000

# Run the app
CMD ["npm", "start"]
