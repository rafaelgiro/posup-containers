FROM node:17-alpine3.14 as builder
ENV NODE_ENV build
USER node
WORKDIR /home/node

COPY package*.json ./
RUN npm install --silent

COPY --chown=node:node . .
RUN npm run build \
  && npm prune --production

# ---

FROM node:17-alpine3.14

ENV NODE_ENV production

USER node
WORKDIR /home/node

COPY --from=builder --chown=node:node /home/node/package*.json ./
COPY --from=builder --chown=node:node /home/node/node_modules/ ./node_modules/
COPY --from=builder --chown=node:node /home/node/dist/ ./dist/

CMD ["node", "dist/main.js"]