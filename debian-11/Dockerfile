FROM debian:bullseye
LABEL maintainer="tsmith84@gmail.com"

ENV DEBIAN_FRONTEND noninteractive
RUN /usr/bin/apt-get update && \
    /usr/bin/apt-get -y install \
    apt-transport-https \
    apt-utils \
    cron \
    curl \
    dbus \
    dirmngr \
    dmidecode \
    gnupg \
    ifupdown \
    iptables \
    iputils-ping \
    kmod \
    locales \
    lsb-release \
    lsof \
    net-tools \
    netcat \
    nmap \
    perl \
    procps \
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
