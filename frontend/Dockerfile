FROM node:16.6.2 as build
WORKDIR /app

COPY . ./

RUN yarn build

CMD cp -r build result_build