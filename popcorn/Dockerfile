FROM archlinux:latest

ARG USERNAME

# setup aur access for $USERNAME
ADD add-aur.sh /usr/sbin/add-aur
RUN add-aur $USERNAME

# Install popcorntime and mpv
RUN su $USERNAME -c "yay -S --noprogressbar --needed --noconfirm pulseaudio popcorntime mpv"

# Disable shared memory for pulseaudio
RUN sed -i "s/; enable-shm = yes/enable-shm = no/g" /etc/pulse/daemon.conf && \
    sed -i "s/; enable-shm = yes/enable-shm = no/g" /etc/pulse/client.conf

USER $USERNAME

ENTRYPOINT ["popcorntime"]
