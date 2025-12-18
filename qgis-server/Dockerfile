FROM qgis/qgis-server:ltr

# Carpeta donde quedará tu proyecto dentro del contenedor
RUN mkdir -p /project

# Copiamos el proyecto QGIS (.qgz) y demás datos al contenedor
COPY data/ /project/

# Configuración de logs (Railway los mostrará en consola)
ENV QGIS_SERVER_LOG_STDERR=1
ENV QGIS_SERVER_LOG_LEVEL=0

# Indicar explícitamente el proyecto QGIS que debe servir QGIS Server
ENV QGIS_PROJECT_FILE=/project/demo_quininde.qgz

# QGIS Server corre detrás de Apache en el puerto 80
EXPOSE 80

