FROM devkitpro/devkitppc

RUN wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb && \
    dpkg -i packages-microsoft-prod.deb && \
    apt-get update && \
    apt-get install -y powershell

RUN wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb && \
    dpkg -i packages-microsoft-prod.deb && \
    rm packages-microsoft-prod.deb && \
    apt-get update && \
    apt-get install -y dotnet-sdk-6.0 libfontconfig1

RUN apt-get update && \
    apt-get install -y ffmpeg libavcodec-dev libavformat-dev libavresample-dev libavutil-dev libswresample-dev libswscale-dev gcc g++

RUN wget https://wit.wiimm.de/download/wit-v3.05a-r8638-x86_64.tar.gz && \
    tar xfz wit-v3.05a-r8638-x86_64.tar.gz && \
    rm wit-v3.05a-r8638-x86_64.tar.gz && \
    cp ./wit-v3.05a-r8638-x86_64/bin/* /bin/ && \
    rm -rf ./wit-v3.05a-r8638-x86_64

RUN cd ~ && \
    git clone https://github.com/haroohie-club/avthp.git && \
    cd avthp && \
    cmake CMakeLists.txt && \
    make && \
    mv avthp /bin/ && \
    cd /