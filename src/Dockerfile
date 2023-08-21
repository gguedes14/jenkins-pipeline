FROM alpine:latest as npm_install

WORKDIR /var/www/app

COPY . .

RUN apk update \
    && apk add nodejs \
    npm

RUN npm install

RUN npm run build

FROM nginx:alpine as final

WORKDIR /usr/share/

RUN apk update && \
    apk upgrade

COPY --from=npm_install /var/www/app/build /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]