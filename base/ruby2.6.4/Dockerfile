FROM ruby:2.6.4
LABEL maintainer="kyoungwon.lee86@gmail.com"

# Install ssh client and git
RUN sed -i 's/archive.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y openssh-client git nodejs postgresql-client && \
    rm -rf /var/lib/apt/lists/*

CMD ["/bin/bash"]
