FROM node:6-alpine
#Utilizar la imagen 6-alpine de node
EXPOSE 3000
#Exponer el puerto 3000
WORKDIR /usr/src/app
#Cambiar a la ruta /usr/src/app
COPY package.json package.json
#Copiar package.json
RUN command apk add --no-cache tini
#Ejecutar el comando RUN  con la siguiente instrucción apk add --no-cache tini
RUN npm install && npm cache clean --force
#Ejecutar el comando RUN  con la siguiente instrucción npm install && npm cache clean --force
COPY . .
#Copiar todo el contenido
CMD [ "/sbin/tini", "--", "node", "./bin/www" ]
#Ejecutar el comando CMD con la siguientes instrucciones "/sbin/tini", "--", "node", "./bin/www"