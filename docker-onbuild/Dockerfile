FROM rails:4.1.1

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
EXPOSE 3000
CMD ["rails", "server"]

# Add Gemfile first for docker caching
ONBUILD ADD Gemfile /usr/src/app
ONBUILD ADD Gemfile.lock /usr/src/app
ONBUILD RUN bundle install --system

ONBUILD ADD . /usr/src/app
