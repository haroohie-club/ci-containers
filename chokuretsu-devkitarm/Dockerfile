FROM devkitpro/devkitarm

RUN wget https://packages.microsoft.com/config/debian/11/packages-microsoft-prod.deb && \
    dpkg -i packages-microsoft-prod.deb && \
    rm packages-microsoft-prod.deb && \
    apt update && \
    apt install -y powershell

RUN apt install -y dotnet-sdk-8.0 libfontconfig1 libopenal1

RUN wget https://haroohie.blob.core.windows.net/ci-containers/xdelta3.zip && \
    unzip xdelta3.zip && \
    rm xdelta3.zip && \
    chmod +x xdelta3 && \
    mv xdelta3 /bin/
