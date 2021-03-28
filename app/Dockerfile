FROM node:14-alpine

# set working directory
WORKDIR /app

# https://github.com/nodejs/docker-node/pull/367#issuecomment-428352379
RUN apk update && \
    apk upgrade && \
    apk add git

# # add `/app/node_modules/.bin` to $PATH
# ENV PATH /app/node_modules/.bin:$PATH

COPY package*.json ./

RUN npm install -g gatsby-cli
RUN npm install
# RUN npm install --silent && mv node_modules ../

# COPY . .

EXPOSE 8000

# USER node

# CMD ["npm", "start"]

# CMD tail -f /dev/null
