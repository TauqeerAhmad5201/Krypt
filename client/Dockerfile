# Use an official Node.js image as the base
FROM node:21-alpine3.18

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install project dependencies
RUN npm install

# Copy the entire project directory into the container
COPY . .

# Build the React app (replace 'build' with your actual build command)
RUN npm run build

# Expose the port where the app will run
EXPOSE 3000

# Define the default command to start the app
CMD ["npm", "run", "serve"]