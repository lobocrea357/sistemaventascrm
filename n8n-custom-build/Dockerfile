# Forzamos la versión basada en Alpine (cambia 'latest' por esta etiqueta)
FROM n8nio/n8n:1.77.2-alpine

USER root

# Ahora sí funcionará apk
RUN apk add --update --no-cache \
    build-base \
    git \
    graphicsmagick

# Librerías de Node
RUN npm install -g axios moment exceljs

USER node
