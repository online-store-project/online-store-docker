FROM node:14

WORKDIR /usr/src/server/

RUN git clone https://github.com/online-store-project/source-code.git ./

RUN npm install

EXPOSE 3000

CMD ["npm", "start"]