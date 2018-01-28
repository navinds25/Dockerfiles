
FROM java-ubuntu-v1

ADD idea-IC-163.10154.41/ /home/intellij/

RUN apt update && apt install -y libxext-dev libxrender-dev libxtst-dev 

RUN useradd -c "intellij user" -m -d /home/intellij -s /bin/bash intellijusr

USER intellijusr

WORKDIR /home/intellij

#CMD /bin/bash
CMD /bin/bash bin/idea.sh
