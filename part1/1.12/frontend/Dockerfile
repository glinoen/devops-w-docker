FROM node:13

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

ENV API_URL=http://localhost:8000

EXPOSE 5000

CMD [ "npm", "start" ]
