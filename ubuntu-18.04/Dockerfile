FROM ubuntu:18.04
LABEL maintainer="sean@sean.io"

ENV DEBIAN_FRONTEND noninteractive
RUN /usr/bin/apt-get update && \
    /usr/bin/apt-get -y install \
    apt-transport-https \
    apt-utils \
    curl \
    dbus \
    cron \
    dirmngr \
    dmidecode \
    gnupg \
    iproute2 \
    iptables \
    iputils-ping \
    kmod \
    linux-base \
    locales \
    lsb-release \
    lsof \
    net-tools \
    netcat \
    nmap \
    perl \
    procps \
    snapd \
    strace \
    sudo \
    systemd \
    tcpdump \
    telnet \
    tzdata \
    udev \
    vim-tiny \
    wget && \
    /usr/bin/apt-get clean && \
    /usr/bin/apt-get -y autoremove && \
    rm -rf /tmp/* /var/tmp/* && \
    sudo ln -s /bin/mkdir /usr/bin/mkdir && \
    rm /etc/systemd/system/getty.target.wants/getty\@tty1.service # Remove annoying tty service which consumes 100% CPU

CMD [ "/bin/systemd" ]
