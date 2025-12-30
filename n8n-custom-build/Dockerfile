# Utiliza la imagen oficial de n8n como base
FROM n8nio/n8n:latest

# Crea un directorio para los nodos personalizados
WORKDIR /home/node/.n8n/custom

# Copia tu package.json al directorio de trabajo
COPY n8n-data/nodes/package.json .

# Cambia al usuario root para instalar los nodos
USER root

# Instala los nodos definidos en package.json
RUN npm install

# Vuelve al usuario 'node' por seguridad
USER node
