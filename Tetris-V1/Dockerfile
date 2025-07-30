# Use the official Node.js 18 image as the base image
FROM node:18

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json (or yarn.lock) to the container
COPY package*.json ./

# Install project dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Build the React app with OpenSSL legacy provider workaround
RUN NODE_OPTIONS=--openssl-legacy-provider npm run build

# Expose the port that the app will run on (default: 3000)
EXPOSE 3000

# Start the React app
CMD ["npm", "start"]
