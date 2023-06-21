FROM node:20

WORKDIR /app

#aptのupdate
RUN apt update

#zenn cliのインストール
RUN npm init --yes \
    && npm install zenn-cli@latest \
    && npx zenn init

COPY ../articles /app/articles
COPY ../images /app/images

CMD [ "npx", "zenn", "preview" ]
