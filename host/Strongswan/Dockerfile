FROM debian:bullseye

# Install StrongSwan
RUN apt-get update && \
    apt-get install -y strongswan && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Copy StrongSwan configuration files
COPY strongswan.conf /etc/strongswan.conf
COPY ipsec.conf /etc/ipsec.conf

# Expose necessary ports
EXPOSE 500/udp 4500/udp

# Start StrongSwan
CMD ["ipsec", "start", "--nofork"]
