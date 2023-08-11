FROM node
LABEL application="IAP" 
LABEL owner="Macko"

WORKDIR /code

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm","start"]

