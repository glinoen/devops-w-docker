FROM node:13

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

ENV FRONT_URL=http://localhost:5000

EXPOSE 8000

CMD [ "npm", "start" ]
