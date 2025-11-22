FROM node:latest

WORKDIR /app

COPY package.json ./

RUN npm install

ARG DEFAULT_PORT=3000

ENV PORT=${DEFAULT_PORT}

COPY . ./

CMD ["node", "server.js"]