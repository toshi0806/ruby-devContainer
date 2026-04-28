FROM ruby:3.4

ENV DISPLAY=host.docker.internal:0.0 \
    LANG=C.UTF-8 \
    TZ=Asia/Tokyo

ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID

RUN apt-get update \
    && apt-get install -y telnet openjdk-21-jdk-headless sudo bash-completion \
    && rm -rf /var/lib/apt/lists/* \
    && groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m -s /bin/bash $USERNAME \
    && echo "$USERNAME ALL=(root) NOPASSWD:ALL" > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME \
    && git config --system --add safe.directory '*' \
    && gem install pry

USER $USERNAME
