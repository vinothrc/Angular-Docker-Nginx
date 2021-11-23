# Stage 1: Compile and Build angular codebase

# Use official node image as the base image
FROM node:16-alpine as build

RUN mkdir -p /app
# Set the working directory
WORKDIR /app

COPY package.* /app

# Add the source code to app
COPY . /app

RUN npm install -g npm
# Install all the dependencies
RUN npm install

# Generate the build of the application
#RUN npm run build
RUN npm run build --prod

# Stage 2: Serve app with nginx server

# Use official nginx image as the base image
FROM nginx:latest

# Copy the build output to replace the default nginx contents.
#COPY --from=build /usr/local/app/dist/sample-angular-app /usr/share/nginx/html
COPY --from=build /app/dist/example1 /var/www/html
