FROM node:20-alpine

RUN apk add --no-cache yarn

WORKDIR /app

COPY ./web/package*.json ./web/yarn.lock* ./

RUN yarn install --frozen-lockfile

COPY ./web .

COPY ./personal-security-checklist.yml ./public/

EXPOSE 5173

CMD ["yarn", "dev", "--host", "10.0.20.30"]