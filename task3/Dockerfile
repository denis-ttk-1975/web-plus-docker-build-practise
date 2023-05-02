FROM node:16-alpine

WORKDIR /home/ilovedocker/app

COPY ./packages/package*.json ./
# Флаг --omit=dev означает - "не ставить devDependencies"
# они не нужны нам в продакшен-окружении
RUN npm i --omit=dev

COPY ./src .

EXPOSE 3032

CMD [ "node", "main.js" ]
