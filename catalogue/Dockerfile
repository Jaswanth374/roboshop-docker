FROM node:20.0
WORKDIR /app
ADD https://roboshop-artifacts.s3.amazonaws.com/catalogue-v3.zip  /tmp
RUN unzip /tmp/catalogue-v3.zip -d /tmp
RUN npm install
ENV MONGO=true \
    MONGO_URL="mongodb:mongodb:27017/catalogue"
CMD ["node", "server.js"]