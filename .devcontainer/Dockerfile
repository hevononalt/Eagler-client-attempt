FROM mcr.microsoft.com/devcontainers/universal:2

# Install necessary packages for VNC and noVNC
RUN apt-get update && apt-get install -y \
    xfce4 \
    xfce4-goodies \
    x11vnc \
    supervisor \
    websockify \
    novnc

# Set password for VNC
RUN x11vnc -storepasswd 1234 /etc/x11vnc.pass

# Command to start VNC server and noVNC
CMD ["/usr/bin/supervisord"]
