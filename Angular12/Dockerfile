### STAGE 1: Build ###
FROM node:12.7-alpine AS build
WORKDIR /usr/src/app
COPY package.json package-lock.json ./
RUN npm install
COPY . /usr/src/app
RUN npm run build

### STAGE 2: Run ###
FROM nginx:latest
#COPY nginx.conf /etc/nginx/nginx.conf
COPY --from=build /usr/src/app/dist /var/www/html
