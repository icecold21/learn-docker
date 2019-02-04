# Specify base image that already have npm
FROM node:alpine

# Put package.json and index.js to the image
COPY ./ ./

# Run
RUN npm install

# Initscript
CMD ["npm", "start"]