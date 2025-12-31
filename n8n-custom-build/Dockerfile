FROM n8nio/n8n:latest

USER root

# Usamos apt-get en lugar de apk
RUN apt-get update && apt-get install -y \
    build-essential \
    git \
    graphicsmagick \
    && rm -rf /var/lib/apt/lists/*

# Instalamos las librerías de Node globales
RUN npm install -g axios moment exceljs

USER node
