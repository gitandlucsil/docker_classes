FROM node as builder
RUN mkdir /app/ && mkdir /publish/
WORKDIR /app/
RUN npm install -g @angular/cli
ADD ./package.json ./
RUN npm install 
ADD ./ ./
RUN ng build --output-path /publish/

FROM nginx
COPY --from=builder /publish /usr/share/nginx/html
