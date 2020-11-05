FROM node:alpine AS my-app-build
WORKDIR /app
COPY ./app/ .
RUN npm ci && npm run build
# RUN ng serve

FROM nginx:alpine
COPY --from=my-app-build /app/dist/app /usr/share/nginx/html
EXPOSE 80