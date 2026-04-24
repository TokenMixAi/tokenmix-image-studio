# ---- Build stage ----
FROM node:20-alpine AS build

WORKDIR /app

ARG VITE_DEFAULT_API_URL
ENV VITE_DEFAULT_API_URL=$VITE_DEFAULT_API_URL

COPY package.json package-lock.json ./
RUN npm ci

COPY . .
RUN npm run build

# ---- Production stage ----
FROM nginx:alpine

COPY --from=build /app/dist /usr/share/nginx/html
COPY deploy/nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
