FROM ruby
RUN	apt-get update -y && apt-get install -y && \
	apt-get install -y nodejs
RUN	gem install rails && \
	cd /opt
ONBUILD EXPOSE 3000
ONBUILD COPY app/ /opt/
WORKDIR	/opt/app
ONBUILD	RUN bundle install && \
			rake db:migrate && \
			rake db:setup && \
			rake db:seed
