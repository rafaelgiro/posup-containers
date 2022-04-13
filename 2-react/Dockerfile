FROM node:17-alpine3.14
WORKDIR /app
COPY package.json ./
RUN npm install --silent
COPY . ./
CMD ["npm", "start"]