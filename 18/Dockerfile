# 元になるイメージを生成
FROM docker/whalesay:latest

# イメージビルドの際に実行する命令
# ubuntuのイメージだからapt-get  fortunesパッケージをインストール
RUN apt-get -y update && apt-get install -y fortunes

# コンテナが作成した後で実行する
CMD /usr/games/fortune | cowsay