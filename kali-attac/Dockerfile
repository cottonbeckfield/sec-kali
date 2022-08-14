# The image for Kali: https://hub.docker.com/r/kalilinux/kali-rolling
FROM kalilinux/kali-rolling

# Perform updates
RUN apt-get -y update && \
    apt-get -y dist-upgrade && \
    apt-get -y autoremove && \
    apt-get clean

# Packages to install on this very basic image.
# Note: You can do: apt update && apt -y install kali-linux-large to
#       go crazy on Kali packages. I prefer the smol image.
RUN apt-get -y install \
    vim \
    git-all \
    net-tools \
    iputils-ping \
    whois \
    python3-pip \
    # Vulnerability Scanners
    dirb \
    wpscan \
    # Sub-domain Enumberation
    amass \
    # Oh, boy, Metasploit, here we go boiiiis.
    metasploit-framework \
    postgresql \
    tor
        # Tor Proxy, for proxying traffic. 
        # Note about Tor: Exit nodes are published and kept track of, which allows for
        #                 some companies to auto-update and block them.

# Get a shell, profit.
ENTRYPOINT ["/bin/bash"]