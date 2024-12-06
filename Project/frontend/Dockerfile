# Use an official Node runtime as a parent image
FROM node:16
# Set the working directory in the container
WORKDIR /app
# Copy package.json and package-lock.json
COPY package*.son ./
# Install app dependencies
RUN npm install
# Copy the current directory contents into the container
copy . .
# Build the app
run npm run build
# Make port 3000 available to the world outside this container
EXPOSE 5000
# Define environment variable
ENV REACT_APP_API_URL=http://localhost:5000/api
ENV REACT_APP_ENV=production
# Run the app when the container launches

CMD ["npm", "start"]