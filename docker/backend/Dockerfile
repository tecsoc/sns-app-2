FROM ruby:3.3.5

RUN apt-get update \
	&& apt-get install -y --no-install-recommends \
		postgresql-client \
	&& rm -rf /var/lib/apt/lists/*

WORKDIR /usr/app
COPY Gemfile* ./
RUN bundle install
# COPY ../backend .

EXPOSE 3000
CMD ["rails", "server", "-b", "0.0.0.0"]