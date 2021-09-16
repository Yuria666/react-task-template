FROM node:lts
WORKDIR /usr/src/client

# ファイルを全部作業用ディレクトリにコピー
COPY ./ /usr/src/client
COPY ./package.json .
COPY ./yarn.lock .

# ポートのエクスポート
EXPOSE 3000

# RUNコマンド:image作成時に実行される
RUN yarn install
# RUN yarn build
# CMD命令はDockerイメージからDockerコンテナを作成するときに実行されます。
# CMD yarn start
