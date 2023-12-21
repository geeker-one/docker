# Kali Linux latest with useful tools by tsumarios
FROM kalilinux/kali-rolling

# Set working directory to /root
WORKDIR /root

COPY sources.list /etc/apt/sources.list

# Update
RUN apt -y update && DEBIAN_FRONTEND=noninteractive apt -y dist-upgrade && apt -y autoremove && apt clean\
    &&apt -y install curl wget neovim git \
    &&apt -y install python3-pip\
    &&DEBIAN_FRONTEND=noninteractive apt -y install kali-tools-top10 man-db\
    &&apt -y install zsh && chsh -s /bin/zsh

ENTRYPOINT ["/bin/zsh"]
