FROM node:alpine as builder
WORKDIR '/app'
COPY ./package.json ./
RUN npm install -g npm@8.1.1
COPY . .
RUN npm run build

FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html