FROM google/nodejs

MAINTAINER Johann Saunier <johann_27@hotmail.fr>

VOLUME ["/app"]
WORKDIR /app

RUN npm install -g bower grunt-cli gulp-cli git mercurial
RUN npm update -g

CMD ["bash"]
