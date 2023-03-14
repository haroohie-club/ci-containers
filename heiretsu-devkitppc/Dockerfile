FROM devkitpro/devkitppc

LABEL "org.haroohie.author"="Haroohie Translation Club"
LABEL version="1.0"
LABEL description="CI container for building the translated Suzumiya Haruhi no Chokuretsu patch"

RUN wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb; \
    dpkg -i packages-microsoft-prod.deb; \
    apt-get update; \
    apt-get install -y powershell;

RUN wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb; \
    dpkg -i packages-microsoft-prod.deb; \
    rm packages-microsoft-prod.deb; \
    apt-get update; \
    sudo apt-get install -y dotnet-sdk-6.0; \
    apt-get install -y libfontconfig1

RUN apt-get update; \
    apt-get install -y ffmpeg; \
    apt-get install -y libavcodec-dev; \
    apt-get install -y libavformat-dev; \
    apt-get install -y libavresample-dev; \
    apt-get install -y libavutil-dev; \
    apt-get install -y libswresample-dev; \
    apt-get install -y libswscale-dev; \
    apt-get install -y gcc; \
    apt-get install -y g++;

RUN cd ~; \
    git clone https://github.com/haroohie-club/avthp.git; \
    cd avthp; \
    cmake CMakeLists.txt; \
    make; \
    mv avthp /; \
    cd /;