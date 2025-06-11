FROM nginx:stable-alpine

# Creamos y usamos un volumen /temp
VOLUME /temp

#Install web app on nginx server
RUN rm -rf /usr/share/nginx/html/*

COPY nginx.conf /etc/nginx/nginx.conf
COPY mime.types /etc/nginx/mime.types

# Copiar el contenido de tu proyecto frontend al contenedor
COPY sistema-ventas-front/ /usr/share/nginx/html/

# Exponer el puerto 80
EXPOSE 80

# Comando para ejecutar nginx en primer plano
CMD ["nginx", "-g", "daemon off;"]
