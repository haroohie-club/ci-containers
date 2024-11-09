FROM devkitpro/devkitarm:latest AS devkitarm

FROM freedesktopsdk/flatpak:latest
COPY --from=devkitarm /opt/devkitpro /opt/devkitpro

RUN groupadd root -g 0 && \
    useradd -ou 0 -g root root

# Install sudo
RUN git clone https://github.com/sudo-project/sudo.git && \
    cd sudo && \
    ./configure --prefix=/usr && \
    make && \
    make install && \
    cd .. && \
    rm -rf sudo