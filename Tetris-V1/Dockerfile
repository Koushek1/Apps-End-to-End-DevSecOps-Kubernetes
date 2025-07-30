# Use official Node.js 16 image (compatible with react-scripts 4.0.3)
FROM node:16

# Set the working directory
WORKDIR /app

# Copy only package.json and package-lock.json for better layer caching
COPY package*.json ./

# Install project dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the React app for production
RUN npm run build

# Expose the port the app will run on (optional if using a web server like nginx externally)
EXPOSE 3000

# Start the app (optional; use this only if you're running a dev server like `react-scripts start`)
# CMD ["npm", "start"]
