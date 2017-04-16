# rpi-docker-named
About a Docker Container and his Named.
(heavily inspired by every rpi named repo)

sudo docker run --name bind -d \
                --restart=always \
                --publish 53:53/tcp \
                --publish 53:53/udp \
                --publish 10000:10000/tcp \
                --volume /srv/docker/bind:/data rpi-docker-named
