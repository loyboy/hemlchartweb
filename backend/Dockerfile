FROM node:14.21.1-slim

# Create app directory
WORKDIR /app

# Also copy the lock file
COPY ./package.json .

# typescript is a devDependencies, no need to separately install it
RUN npm install

# Copy the rest of your application in
# (include `node_modules` in a `.dockerignore` file)
COPY ./ ./

# copy files from host to container
# COPY . .

# Build the nodejs app
RUN npx tsc -p .

# Expose the port the app runs on
EXPOSE 8080

# Serve the built app
CMD ["npm", "start"]





