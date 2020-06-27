FROM ruby:2.3.3
# build-essential コンパイラなど、ビルドに必要　libpq-dev　postgresqlへの接続に必要
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN mkdir /myapp
WORKDIR /myapp
COPY Gemfile /myapp/Gemfile
COPY Gemfile.lock /myapp/Gemfile.lock
# bundleコマンドは FROM に指定したrubyのイメージに存在する
RUN bundle install
COPY . /myapp