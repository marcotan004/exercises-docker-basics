FROM ubuntu:24.04

EXPOSE 5001

WORKDIR /usr/src/app

RUN apt-get update && apt install -y curl
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
RUN apt install -y nodejs

COPY package.json package-lock.json ./
RUN npm ci
RUN npm install -g serve

COPY . .
RUN npm run build

CMD ["serve", "-s", "-l", "5001", "build"]