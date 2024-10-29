FROM debian:bookworm

# Install StrongSwan and Nginx
RUN apt-get update && \
    apt-get install -y strongswan nginx && \
    rm -rf /var/lib/apt/lists/*

# Copy StrongSwan configuration files
COPY ipsec.conf /etc/strongswan/ipsec.conf
COPY ipsec.secrets /etc/strongswan/ipsec.secrets

# Copy Nginx configuration
COPY nginx.conf /etc/nginx/sites-available/default

# Expose ports
EXPOSE 80 500 4500

# Start both Nginx and StrongSwan
CMD service nginx start && ipsec start --nofork
