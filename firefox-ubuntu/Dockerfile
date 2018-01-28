FROM ubuntu

RUN apt update && apt install -y firefox

RUN useradd -c "Firefox user" -m -d /home/firefox -s /bin/bash firefoxusr

USER firefoxusr

CMD firefox

