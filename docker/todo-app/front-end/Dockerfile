FROM node:14-alpine AS todofrontend
WORKDIR /app
COPY package*.json ./
ADD node_modules.tar.gz ./

COPY . .

EXPOSE 3000

CMD [ "npm", "start"]

RUN npm run build

FROM nginx:1.21.3-alpine-perl
COPY --from=todofrontend /app/build /usr/share/nginx/html
