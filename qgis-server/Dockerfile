FROM qgis/qgis-server:ltr

# Carpeta donde quedará tu proyecto dentro del contenedor
RUN mkdir -p /project

# Copiamos el .qgz al contenedor
COPY data/ /project/

# Logs a stderr (útil en Railway)
ENV QGIS_SERVER_LOG_STDERR=1
ENV QGIS_SERVER_LOG_LEVEL=0

# QGIS Server en esta imagen suele correr detrás de Apache y expone 80 internamente.
# Railway hace el proxy al puerto del contenedor, así que no necesitas hardcodear $PORT aquí.
EXPOSE 80
