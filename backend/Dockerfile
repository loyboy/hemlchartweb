FROM node:14.21.1-alpine3.15

# Create app directory
WORKDIR /usr/src/app

# copy files from host to container
COPY . .

RUN npm install

# Build the nodejs app
RUN npm run build

# Expose the port the app runs on
EXPOSE 8080

# Serve the built app
CMD ["npm", "start"]





