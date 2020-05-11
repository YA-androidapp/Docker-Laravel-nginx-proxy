FROM nginx

ADD ./server.conf /etc/nginx/conf.d/default.conf
ADD ./public/index.html /root/public/index.html

RUN mkdir /root/logs
RUN chmod 755 -R /root

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
