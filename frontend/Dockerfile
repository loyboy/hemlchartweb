FROM node:14.21.1-slim as builder

# Create app directory
WORKDIR /usr/src/app

COPY . .

# Install app dependencies
RUN npm install

# Build the angular app
RUN npm run build

### STAGE 2 ###
FROM nginx:1.16.1-alpine
COPY --from=builder /usr/src/app/www /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]





