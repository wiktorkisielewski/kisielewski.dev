FROM nginx:1.23.0

COPY  conf/nginx.conf /etc/nginx/nginx.conf

RUN apt update \ 
    && apt install git curl vim --assume-yes

RUN cd /etc/nginx \
    && git clone https://github.com/wiktorkisielewski/kisielewski.dev.git

CMD service nginx start && cd /etc/nginx/kisielewski.dev && while :; do git reset --hard HEAD && git pull && sleep 60; done