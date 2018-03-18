#Create container and install necessary stuffs
FROM			ruby
RUN				apt-get update -y && apt-get install -y && \
				apt-get install -y nodejs
RUN				gem install rails && \
				cd /opt && \
				rails new app
#Inside container, copy whatever is needed and start up rails
ONBUILD EXPOSE	3000
ONBUILD RUN		bundle install && \
				rake db:migrate && \
				rake db:setup && \
				rake db:seed

#Sets workdirapt 
WORKDIR			/opt/app