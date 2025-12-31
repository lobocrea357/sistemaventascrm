FROM n8nio/n8n:latest

USER root

# Usamos apt-get porque la imagen latest es Debian
RUN apt-get update && apt-get install -y \
    build-essential \
    git \
    graphicsmagick \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Instalamos tus librerías de Node
RUN npm install -g axios moment exceljs

USER node
