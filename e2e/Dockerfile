FROM cypress/included:10.0.1

RUN apt install curl && curl -f https://get.pnpm.io/v6.16.js | node - add --global pnpm

WORKDIR /e2e

COPY pnpm-lock.yaml ./
RUN pnpm fetch

COPY package.json ./
RUN pnpm install -r --offline
