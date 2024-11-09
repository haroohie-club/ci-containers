FROM devkitpro/devkitarm:latest AS devkitarm

FROM freedesktopsdk/flatpak:latest
COPY --from=devkitarm /opt/devkitpro /opt/devkitpro

RUN groupadd root -g 0 && \
    useradd -ou 0 -g root vsts_azpcontainer