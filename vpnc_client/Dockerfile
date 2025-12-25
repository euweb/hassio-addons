ARG BUILD_FROM
FROM $BUILD_FROM

RUN apk add --update vpnc

# Copy root filesystem
COPY rootfs /

# Make vpnc-script executable
RUN chmod +x /etc/vpnc/vpnc-script-no-default-route
