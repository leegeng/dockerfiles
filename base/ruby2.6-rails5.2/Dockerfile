FROM ruby:2.6
LABEL maintainer="kyoungwon.lee86@gmail.com"

# Install ssh client and git
RUN sed -i 's/archive.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y openssh-client git nodejs postgresql-client sqlite3 vim && \
    rm -rf /var/lib/apt/lists/* && \
    gem install rails -v 5.2

CMD ["/bin/bash"]
