FROM node:20-alpine

WORKDIR /app

COPY . .

RUN yarn install

CMD ["node", "./bin/www"]