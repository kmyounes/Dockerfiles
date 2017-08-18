FROM ubuntu
MAINTAINER KASMI Mohamed Younes <kmyounes@protonmail.com>

RUN  sh -c 'echo "deb http://repository.spotify.com stable non-free" >> /etc/apt/sources.list.d/spotify.list' \
     &&  apt-key adv --keyserver keyserver.ubuntu.com --recv-keys D2C19886 \
     && apt-get update \
     &&  apt-get install -y spotify-client --no-install-recommends \
	 && rm -rf /var/lib/apt/lists/*


COPY configs/asoundrc /root/.asoundrc

CMD ["spotify"]
