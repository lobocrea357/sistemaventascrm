# 1. Usamos una base Node.js Alpine pura (tú controlas el OS)
FROM node:22-alpine

# 2. Instalamos dependencias de sistema (como es Alpine estándar, apk SÍ funciona)
RUN apk add --update --no-cache \
    python3 \
    py3-pip \
    ffmpeg \
    git \
    build-base \
    graphicsmagick \
    curl \
    tini

# 3. Instalamos n8n y tus librerías globales
#    -g instala n8n como comando global
RUN npm install -g n8n axios moment exceljs

# 4. Configuración de entorno requerida para n8n
ENV NODE_ENV=production
ENV GENERIC_TIMEZONE=America/Caracas
ENV TZ=America/Caracas
# Habilitar uso de librerías externas en el nodo Code
ENV NODE_FUNCTION_ALLOW_EXTERNAL=*
ENV NODE_FUNCTION_ALLOW_BUILTIN=*

# 5. Directorio de trabajo y permisos
WORKDIR /home/node
USER node

# 6. Puerto y Comando de inicio
# Tini gestiona los procesos correctamente en contenedores (evita zombies)
ENTRYPOINT ["/sbin/tini", "--"]
CMD ["n8n"]
