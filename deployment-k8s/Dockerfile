FROM nginx:1.23.0

COPY  conf/nginx.conf /etc/nginx/nginx.conf

RUN apt update \ 
    && apt install git curl vim --assume-yes

CMD service nginx start && cd /etc/nginx && git clone https://github.com/wiktorkisielewski/kisielewski.dev.git &&  cd kisielewski.dev && while :; do git reset --hard HEAD && git pull && sleep 600; done