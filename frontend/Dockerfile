FROM node:14.21.1-slim

# Create app directory
WORKDIR /usr/src/app

COPY . .

# Install app dependencies
RUN npm install

# Build the angular app
RUN npm run build

# Expose the port the app runs on
EXPOSE 4200

# Serve the built app
CMD ["npm", "start"]





