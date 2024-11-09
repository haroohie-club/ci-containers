FROM devkitpro/devkitarm:latest AS devkitarm

FROM freedesktopsdk/flatpak:latest
COPY --from=devkitarm /opt/devkitpro /opt/devkitpro