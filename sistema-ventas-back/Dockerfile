# Usar la imagen de node:18.17.1-alpine
FROM node:18.17.1-alpine

# Crear un volumen en /usr/src/app
WORKDIR /usr/src/app

# Copiar los archivos package
COPY package*.json .

# Ejecutar npm install
RUN npm install

# Copiar todo el contenido al contenedor
COPY . .

# Exponer el puerto 3000
EXPOSE 3000

# Ejecutar en el CMD el comando node index.js
CMD ["node", "index.js"]