FROM node:16.6.2 as build
WORKDIR /app
#COPY package*.json ./
#RUN npm install
COPY . ./
#RUN npm run build
#CMD cp -r build result_build

#COPY . ./
RUN yarn build
CMD cp -r build result_build

#FROM node:lts as builder
#
#WORKDIR /code
#
#COPY . .
#
#RUN yarn install \
#  --prefer-offline \
#  --frozen-lockfile \
#  --non-interactive \
#  --production=false
#
#RUN yarn build
#
#RUN rm -rf node_modules && \
#  NODE_ENV=production yarn install \
#  --prefer-offline \
#  --pure-lockfile \
#  --non-interactive \
#  --production=true
#
#FROM node:lts
#
#WORKDIR /code
#
#COPY --from=builder /code  .
#
#ENV HOST 0.0.0.0
#EXPOSE 3000
#
#CMD [ "npm", "start" ]