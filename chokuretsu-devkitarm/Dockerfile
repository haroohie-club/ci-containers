FROM devkitpro/devkitarm

LABEL org.opencontainers.image.authors="Haroohie Translation Club"
LABEL org.opencontainers.image.vendor="Haroohie Translation Club"
LABEL org.opencontainers.image.source=https://github.com/haroohie-club/ci-containers
LABEL org.opencontainers.image.url=https://github.com/haroohie-club/ci-containers
LABEL org.opencontainers.image.version=main
LABEL org.opencontainers.image.title="Chokuretsu CI"
LABEL org.opencontainers.image.description="CI container for building the translated Suzumiya Haruhi no Chokuretsu patch"
LABEL org.opencontainers.image.licenses=AGPL-3.0

RUN wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb; \
    dpkg -i packages-microsoft-prod.deb; \
    apt-get update; \
    apt-get install -y powershell;

RUN wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb; \
    dpkg -i packages-microsoft-prod.deb; \
    rm packages-microsoft-prod.deb; \
    apt-get update; \
    sudo apt-get install -y dotnet-sdk-6.0; \
    apt-get install -y libfontconfig1;

RUN wget https://haroohie.blob.core.windows.net/ci-containers/xdelta3.zip; \
    unzip xdelta3.zip; \
    chmod +x xdelta3; \
    rm xdelta3.zip;
