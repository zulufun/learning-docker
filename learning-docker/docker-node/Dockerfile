FROM node:20-alpine
# same as mkdir /app && cd /app
WORKDIR /app 

COPY . .

RUN npm install

CMD ["npm", "start"]
#alpine để cài package/thư viện ta dùng apk add chứ không phải apt-get như trên Ubuntu nữa