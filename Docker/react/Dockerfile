FROM node:20-alpine

WORKDIR /app

COPY SmartPay-MVP/package*.json ./

RUN npm install

COPY SmartPay-MVP ./

EXPOSE 3000

CMD ["npm", "start"]
