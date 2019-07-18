FROM alexsuch/angular-cli as angular-build
EXPOSE 4200
WORKDIR /build
COPY ./poolmanage-ui .
RUN NG_CLI_ANALYTICS=ci npm install
RUN ng build

FROM nginx:alpine
EXPOSE 80
WORKDIR /app
COPY --from=angular-build /build/dist/poolmanger-ui .
COPY nginx.conf /etc/nginx/nginx.conf


