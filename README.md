# rpi-docker-named
About a Docker Container and his Named.
(heavily inspired by every rpi named repo)

Bla

Goal was to provide a dockerized nameserver for a raspberry pi with raspbian lite and docker.
The host uses the shared path /srv/docker/bind to share bind config files.

        db.192
        db.na.logen
        named.conf.local

Blub

sudo docker run --name bind -d \
                --restart=always \
                --publish 53:53/tcp \
                --publish 53:53/udp \
                --publish 10000:10000/tcp \
                --volume /srv/docker/bind:/data rpi-docker-named
                

