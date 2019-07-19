FROM node:10-alpine as node-build
EXPOSE 8080
WORKDIR /api
COPY ./poolmanager-api .
RUN npm install
ENTRYPOINT ["node", "index.js"]
