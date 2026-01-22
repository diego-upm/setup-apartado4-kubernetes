FROM openliberty/open-liberty:kernel-slim-java8-openj9

WORKDIR /opt/ol

# Configuración del servidor
COPY reviews-wlpcfg/servers /opt/ol/wlp/usr/servers

# WAR generado por Gradle
COPY reviews-application/build/libs/*.war \
     /opt/ol/wlp/usr/servers/defaultServer/apps/

EXPOSE 9080

CMD ["/opt/ol/wlp/bin/server", "run", "defaultServer"]
