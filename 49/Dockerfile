# Djangoの実行環境用のイメージビルドの設定

# python3の実行環境のイメージ名
FROM python:3
# pythonの標準出力、標準エラー出力をバッファーにため込まないための環境変数
ENV PYTHONUNBUFFERED 1
# codeディレクトリの作成
RUN mkdir /code
# 作業ディレクトリをcodeディレクトリに設定
WORKDIR /code
# ビルドコンテキスト上に存在するrequirements.txtをcodeディレクトリにコピー
COPY requirements.txt /code/
# パッケージのインストールを実行
RUN pip install -r requirements.txt
# ビルドコンテキスト内の情報を全てcodeディレクトリにコピー
COPY . /code/