FROM node:14-alpine AS todobackend
WORKDIR /
COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 3001

CMD [ "npm", "start"]