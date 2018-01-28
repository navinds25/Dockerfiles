FROM ubuntu

RUN apt update && apt install squid -y \
&& adduser --system --disabled-password --disabled-login squidusr && \
chown -R squidusr /var/log/squid/

USER squidusr

CMD ["squid"]
