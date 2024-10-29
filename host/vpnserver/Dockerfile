FROM debian:bookworm

RUN apt-get update && \
    apt-get install -y strongswan && \
    rm -rf /var/lib/apt/lists/*

COPY ipsec.conf /etc/strongswan/ipsec.conf
COPY ipsec.secrets /etc/strongswan/ipsec.secrets

CMD ["ipsec", "start", "--nofork"]
