
FROM node:12.22.5-alpine3.14
WORKDIR /app
COPY package*.json ./
RUN npm install --no-optional
COPY . .
EXPOSE 3000
CMD ["npm", "start"]