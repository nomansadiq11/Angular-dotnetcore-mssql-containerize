FROM node:alpine AS my-app-build
WORKDIR /app
COPY ./app/ .
RUN npm ci && npm run build
RUN ng serve