FROM google/nodejs

MAINTAINER Johann Saunier <johann_27@hotmail.fr>

RUN DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get upgrade -y 
RUN apt-get install -y git mercurial ssh
RUN npm install -g bower grunt-cli gulp-cli

#ssh
RUN mkdir /root/.ssh
ADD ssh/id_rsa /root/.ssh/id_rsa
RUN ssh-keyscan -t rsa,dsa github.com >> /root/.ssh/known_hosts

VOLUME ["/app"]
WORKDIR /app

CMD ["bin/entry_point"]
