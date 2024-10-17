FROM node:18-alpine

WORKDIR /app

RUN npm install -g pm2

RUN chown -R node:node /app

USER node

COPY ["package.json", "package-lock.json*", "./"]

RUN npm install --production --silent

COPY --chown=node:node . .

CMD ["pm2-runtime", "ecosystem.config.js", "--env", "production"]