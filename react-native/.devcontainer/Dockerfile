ARG VARIANT="3.12"

FROM mcr.microsoft.com/vscode/devcontainers/base:0-alpine-${VARIANT}

ENV NODE_VERSION=15.5.0
ENV YARN_VERSION=1.22.10

RUN apk update \
    && apk add --no-cache zsh zsh-autosuggestions curl
RUN echo "source /usr/share/zsh/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh" >> ~/.zshrc
RUN apk add --no-cache nodejs npm
RUN npm i -g n expo-cli yarn@$YARN_VERSION
RUN n $NODE_VERSION
