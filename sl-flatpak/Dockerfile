FROM devkitpro/devkitarm:latest AS devkitarm

FROM freedesktopsdk/flatpak:latest
COPY --from=devkitarm /opt/devkitpro /opt/devkitpro

RUN groupadd root -g 0 && \
    useradd -ou 0 -g root user && \
    touch /etc/sudoers && \
    flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo