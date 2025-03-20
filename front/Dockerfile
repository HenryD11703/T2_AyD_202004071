FROM node:18-alpine AS build-stage

WORKDIR /app

COPY package*.json ./

RUN npm install -g typescript vue-tsc

COPY . .

RUN npm run build

FROM nginx:1.21.3-alpine as production-stage

COPY --from=build-stage /app/dist /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]