FROM node:lts

WORKDIR /app

COPY package.json yarn.lock ./

RUN yarn --frozen-lockfile --network-timeout 600000 && yarn cache clean

ENV NODE_ENV=production

COPY . .

RUN yarn build

EXPOSE 1337

CMD ["yarn", "start"]