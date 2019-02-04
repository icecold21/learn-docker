# Specify base image that already have npm
FROM node:alpine

# Set the current working directory
WORKDIR /usr/app

# Put package.json and index.js to the image
COPY ./package.json ./
RUN npm install
COPY ./ ./

# Initscript
CMD ["npm", "start"]