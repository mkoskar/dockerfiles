FROM archlinux

RUN pacman -Syyu --noconfirm && \
    pacman -S --noconfirm mongodb mongodb-tools && \
    rm -rf /var/cache/pacman/pkg/*

VOLUME /var/lib/mongodb

EXPOSE 27017

USER mongodb

ENTRYPOINT ["/usr/bin/mongod", "--dbpath=/var/lib/mongodb"]
