FROM debian:bullseye-slim

RUN groupadd --gid 1000 node \
  && useradd --uid 1000 --gid node --shell /bin/bash --create-home node

# Installation des dépendances
RUN apt update && apt install zsh vim curl nodejs npm yarn git wget apache2 -y

ENV NODE_VERSION 19.8.1

# Affichage des versions installées
RUN node --version \
  && npm --version

RUN yarn --version

# Lancement du serveur apache
RUN service apache2 start