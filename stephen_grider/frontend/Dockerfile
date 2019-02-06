FROM node:alpine as builder
WORKDIR '/app'
COPY package.json ./
RUN npm install terser@3.14.1 --save-dev .
RUN npm install
COPY . .
RUN npm run build

FROM nginx
# Expose command looked by elasticbeanstalk, in local this means nothing
EXPOSE 80
COPY --from=builder /app/build /usr/share/nginx/html
