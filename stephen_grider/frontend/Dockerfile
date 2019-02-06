FROM node:alpine as builder
WORKDIR '/app'
COPY package.json .
RUN npm install terser@3.14.1 --save-dev .
RUN npm install
COPY . .
RUN npm run build

FROM nginx
COPY --from=builder /app/build /usr/share/nginx/html
