FROM node:14.14.0-alpine
WORKDIR "/app"
COPY ./package.json ./
RUN npm install -g npm@8.1.1
COPY . .
CMD ["npm", "run", "start"]