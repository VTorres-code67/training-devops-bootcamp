FROM node:20-alpine

# Creamos el directorio de la app
WORKDIR /app

# Copiamos los archivos de dependencias
COPY package*.json ./

# Instalamos todo (sin caché para evitar errores previos)
RUN npm install

# Copiamos el resto del código (incluyendo la carpeta src que ya tienes)
COPY . .

# Exponemos el puerto de la app
EXPOSE 3001

# Arrancamos la aplicación
CMD ["node", "src/index.js"]
