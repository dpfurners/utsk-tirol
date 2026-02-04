FROM node:20-bookworm-slim

WORKDIR /app

ENV STRAPI_URL=http://strapi:1337

COPY package.json ./

RUN npm install

COPY . .

EXPOSE 4321

CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0", "--port", "4321"]
