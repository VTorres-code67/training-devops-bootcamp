FROM node:20-alpine
WORKDIR /app

# Copiamos los archivos de configuración
#COPY package.json ./


# TRUCO: Como el servidor no tiene internet, saltamos el paso de RUN npm install
# y asumimos que usaremos los archivos que ya tienes en tu carpeta local.

COPY . .

EXPOSE 3001

#HEALTHCHECK --interval=30s --timeout=5s --retries=3 \
 # CMD wget --quiet --tries=1 --spider http://localhost:3001/health || exit 1

CMD ["node", "src/index.js"]
