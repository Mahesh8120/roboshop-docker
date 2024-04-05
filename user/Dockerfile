FROM node:18-alpine3.18
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
WORKDIR /opt/server
RUN chown roboshop:roboshop /opt/server
USER roboshop
ENV MONGO=true
COPY package.json /opt/server
COPY server.js /opt/server
RUN npm install
CMD ["node", "server.js"]