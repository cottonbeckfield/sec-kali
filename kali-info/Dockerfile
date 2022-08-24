# The image for Kali: https://hub.docker.com/r/kalilinux/kali-rolling
FROM kalilinux/kali-rolling

# Perform updates
RUN apt-get -y update --fix-missing && \
    apt-get -y dist-upgrade && \
    apt-get -y autoremove && \
    apt-get clean

# Packages to install on this very basic image.
# Note: You can do: apt update && apt -y install kali-linux-large to
#       go crazy on Kali packages. I prefer the smol image.
RUN apt-get -y install \
    vim \
    git-all \
    # Install network tools
    net-tools \
    nmap \
    iputils-ping \
    whois \
    dnsutils \
    dnsenum \
    dnsmap \
    dnstracer \
    lbd \ 
    tcpdump \
    amap \
    hping3 \
    # Tor Proxy, for proxying traffic. 
    # Note about Tor: Exit nodes are published and kept track of, which allows for
    #                 some companies to auto-update and block them.
    tor
    

# Get a shell, profit.
ENTRYPOINT ["/bin/bash"]