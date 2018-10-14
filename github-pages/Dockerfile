FROM ruby:alpine

WORKDIR /usr/src/app

COPY Gemfile* ./

RUN apk --update add build-base \
  && bundle install \
  && rm -rf /usr/lib/ruby/gems/*/cache/*.gem

CMD ["jekyll", "serve", "--watch", "--force_polling"]
