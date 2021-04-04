FROM node:14

RUN mkdir /root/.ssh/

ADD id_rsa /root/.ssh/id_rsa

RUN touch /root/.ssh/known_hosts

RUN ssh-keyscan github.com >> /root/.ssh/known_hosts

WORKDIR /usr/src/server/

RUN git clone git@github.com:online-store-project/source-code.git ./

RUN mkdir ./frontend-source/images/

COPY ./images ./frontend-source/images/

RUN npm install

EXPOSE 3000

CMD ["npm", "start"]
