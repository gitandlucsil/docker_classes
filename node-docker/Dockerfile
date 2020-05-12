FROM node:alpine

COPY ./ /APP

WORKDIR /APP

RUN npm install 

ENTRYPOINT [ "node" ]

CMD ["/APP/app.js"]