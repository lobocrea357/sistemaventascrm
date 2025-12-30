# Utiliza la imagen oficial de n8n como base
FROM n8nio/n8n:latest

# Crea un directorio para los nodos personalizados
WORKDIR /home/node/.n8n/custom

# Copia primero el package.json para aprovechar el cache de Docker
COPY n8n-data/nodes/package.json .

# Cambia al usuario root para instalar dependencias
USER root
RUN npm install

# Copia el resto de los archivos de nodos (si tienes)
# Si no tienes archivos .js/.ts en n8n-data/nodes/, puedes borrar la siguiente línea
COPY n8n-data/nodes/ .

# Vuelve al usuario 'node' por seguridad
USER node
