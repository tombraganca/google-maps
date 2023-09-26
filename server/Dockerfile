FROM node:20-slim

RUN apt update && apt install -y openssl procps

WORKDIR /home/node/app

COPY package*.json ./

COPY ./ .

RUN npm install

EXPOSE 3000

USER node

CMD npx prisma generate && npm run start:dev


