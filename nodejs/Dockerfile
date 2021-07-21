FROM node:14

WORKDIR /node-server

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3001

CMD ["node", "server.js"]