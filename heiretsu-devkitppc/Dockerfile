FROM devkitpro/devkitppc

RUN echo "deb http://deb.debian.org/debian-security bullseye-security main" > /etc/apt/sources.list.d/bullseye.list

RUN wget https://packages.microsoft.com/config/debian/12/packages-microsoft-prod.deb && \
    dpkg -i packages-microsoft-prod.deb && \
    rm packages-microsoft-prod.deb && \
    apt update && \
    apt install -y powershell

RUN apt install -y build-essential cmake dotnet-sdk-10.0 libfontconfig1 ffmpeg libavcodec-dev libavformat-dev libavutil-dev libswresample-dev libswscale-dev gcc g++ libevdev-dev libusb-1.0-0-dev libxrandr-dev libxi-dev libpangocairo-1.0-0 qt6-base-private-dev libqt6svg6-dev libbluetooth-dev libasound2-dev libpulse-dev libgl1-mesa-dev libcurl4-openssl-dev

RUN apt install -y libudev-dev libsystemd-dev || apt install -y libeudev-dev

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
    cd / && \
    rm -rf ~/avthp

RUN cd ~ && \
    git clone https://github.com/dolphin-emu/dolphin.git && \
    cd dolphin && \
    git submodule update --init --recursive && \
    mkdir build && \
    cd build && \
    cmake .. && \
    (make -j $(nproc) || make -j $(nproc)) && \
    make install && \
    cd / && \
    rm -rf ~/dolphin
