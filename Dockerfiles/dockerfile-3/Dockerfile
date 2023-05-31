
FROM node:14

WORKDIR /app/atom/

COPY requirements.txt .

RUN apt-get update && install python3 && \
    pip install -r requirements.txt

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm","start"]



