FROM node:20-bookworm-slim

WORKDIR /app

RUN apt-get update && apt-get install -y --no-install-recommends \
  build-essential \
  python3 \
  && rm -rf /var/lib/apt/lists/*

COPY package.json yarn.lock ./

RUN corepack enable && yarn install

COPY . .

EXPOSE 1337

CMD ["yarn", "develop"]
