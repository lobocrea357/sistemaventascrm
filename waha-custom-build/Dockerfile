# Utiliza la imagen oficial de waha como base
FROM devlikeapro/waha:latest

# Cambia al usuario root para poder instalar paquetes o realizar cambios
USER root

# A partir de aquí puedes agregar tus personalizaciones.
# Por ejemplo, para instalar alguna dependencia del sistema:
# RUN apt-get update && apt-get install -y <nombre-del-paquete>

# O para copiar algún script personalizado a la imagen:
# COPY ./mi-script.sh /usr/local/bin/mi-script.sh
# RUN chmod +x /usr/local/bin/mi-script.sh

# Es una buena práctica volver a un usuario sin privilegios si es posible,
# aunque para waha puede ser necesario mantenerse como root dependiendo
# de las operaciones que realice.
# USER 1001
