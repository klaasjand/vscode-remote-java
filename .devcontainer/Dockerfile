ARG DOCKER_IMAGE=debian:stable-slim
FROM ${DOCKER_IMAGE}
LABEL maintainer="Klaas Jan Dijksterhuis"

ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID

# Create a user
RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
        curl \
        git \
        maven

# Remove or comment out to use root user
USER $USERNAME
