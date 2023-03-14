FROM devkitpro/devkitarm

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
