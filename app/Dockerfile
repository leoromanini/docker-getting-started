FROM node:12-alpine
RUN apk add --no-cache python g++ make
WORKDIR /app
COPY package.json yarn.lock ./
RUN yarn install --production
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]