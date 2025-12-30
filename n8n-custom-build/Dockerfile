FROM n8nio/n8n:latest

USER root

# Instalamos solo lo necesario para compilar paquetes de Node nativos
# 'build-base' y 'git' son vitales si algun dia haces npm install de algo complejo
# 'graphicsmagick' sirve si usas el nodo de edición de imágenes de n8n
RUN apk add --update --no-cache \
    build-base \
    git \
    graphicsmagick

# (Opcional) Instala aquí las librerías de npm que quieras disponibles globalmente
# Ejemplo: si usas mucho axios, moment o exceljs en tus funciones
RUN npm install -g axios moment exceljs

USER node
