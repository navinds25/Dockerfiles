FROM ubuntu

ENV DEBFILE code_1.18.1-1510857349_amd64.deb

ADD "$DEBFILE" /opt/

RUN apt-get update && apt-get -y install \
	code \
	libasound2 \
	libatk1.0-0 \
	libcairo2 \
	libcups2 \
	libexpat1 \
	libfontconfig1 \
	libfreetype6 \
	libgtk2.0-0 \
	libpango-1.0-0 \
	libx11-xcb1 \
	libxcomposite1 \
	libxcursor1 \
	libxdamage1 \
	libxext6 \
	libxfixes3 \
	libxi6 \
	libxrandr2 \
	libxrender1 \
	libxss1 \
	libxtst6 \
	--no-install-recommends \
        && dpkg -i /opt/"$DEBFILE" && apt-get install -f \
	&& rm -rf /var/lib/apt/lists/*


RUN adduser --system --disabled-password --disabled-login --shell /bin/bash nodeusr

USER nodeusr

WORKDIR /home/nodeusr

ENTRYPOINT code

CMD ["/bin/bash"]
