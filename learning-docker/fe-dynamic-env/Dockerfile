FROM node:20-alpine as build-stage
WORKDIR /app
COPY package.json yarn.lock* ./
RUN yarn --frozen-lockfile
COPY . .
RUN yarn build

FROM nginx:1.25-alpine
COPY --from=build-stage /app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]