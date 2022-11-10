FROM node:17-alpine

RUN mkdir -p /usr/src/nuxt-app
WORKDIR /usr/src/nuxt-app
COPY ./frontend .

RUN npm ci && npm cache clean --force
RUN npm run build

ENTRYPOINT ["node", ".output/server/index.mjs"]
