FROM node:16-alpine3.14
RUN apk add --no-cache python3
RUN apk add --no-cache make gcc g++ linux-headers udev libexecinfo-dev libexecinfo
WORKDIR /app
COPY ./package.json ./
RUN yarn install
COPY ./upload-server ./upload-server
EXPOSE 3854
CMD ["yarn", "start:radio:uploader"]