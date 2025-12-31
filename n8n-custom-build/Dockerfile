# Usamos la imagen oficial
FROM n8nio/n8n:latest

# Cambiamos a root para instalar paquetes
USER root

# Instalamos dependencias del sistema (apk funciona porque la oficial es Alpine)
# graphicsmagick y build-base son vitales
RUN apk add --update --no-cache \
    build-base \
    git \
    graphicsmagick \
    curl

# Instalamos las librerías globales de Node que pediste
RUN npm install -g axios moment exceljs

# Volvemos al usuario node por seguridad (Requisito de Cloud Run para no romper permisos)
USER node
