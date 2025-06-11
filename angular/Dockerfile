# Usar la imagen de nginx:stable-alpine
FROM nginx:stable-alpine

# Crear el volumen /temp
VOLUME /temp

# Borrar los archivos de nginx
RUN rm -rf /usr/share/nginx/html/*

# Copiar los archivos hacia el contenedor
COPY nginx.conf /etc/nginx/nginx.conf
COPY mime.types /etc/nginx/mime.types

# Copiar los archivos del front
COPY sistema-ventas-front/ /usr/share/nginx/html/

# Exponer el puerto 80
EXPOSE 80

# Ejecutar en el CMD el comando nginx -g daemon off;
CMD ["nginx", "-g", "daemon off;"]
