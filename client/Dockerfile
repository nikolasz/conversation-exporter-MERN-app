# client/Dockerfile

FROM node:14

# Set the working directory in the container to /usr/src/app
WORKDIR /usr/src/app

# Copy package.json and package-lock.json into the root directory of the container
COPY package*.json ./

# Install the app dependencies
RUN npm install

# Bundle the app source inside the Docker image
COPY . .

# Expose port 3000 to have it mapped by Docker daemon
EXPOSE 3000

# Define the command to run the app
CMD [ "npm", "start" ]
