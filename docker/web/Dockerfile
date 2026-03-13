FROM node:12.22.8-alpine3.13

ENV NODE_ENV=development

RUN apk --no-cache add yarn python2 make gcc g++

COPY start.sh /start.sh
RUN sed -i 's/\r$//' /start.sh && chmod +x /start.sh

WORKDIR /web

CMD ["sh", "/start.sh"]