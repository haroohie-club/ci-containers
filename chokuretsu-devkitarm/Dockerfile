FROM devkitpro/devkitarm

RUN wget https://packages.microsoft.com/config/debian/12/packages-microsoft-prod.deb && \
    dpkg -i packages-microsoft-prod.deb && \
    rm packages-microsoft-prod.deb && \
    apt update && \
    apt install -y powershell

RUN apt install -y dotnet-sdk-8.0 libfontconfig1 libopenal1 python3-distutils

RUN wget https://haroohie.nyc3.cdn.digitaloceanspaces.com/bootstrap/ci-containers/xdelta3.zip && \
    unzip xdelta3.zip && \
    rm xdelta3.zip && \
    chmod +x xdelta3 && \
    mv xdelta3 /bin/

RUN wget https://bootstrap.pypa.io/pip/3.7/get-pip.py && \
    python ./get-pip.py && \
    pip install boto3