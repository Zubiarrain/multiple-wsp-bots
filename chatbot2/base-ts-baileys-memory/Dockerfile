# Usar imagen oficial de Node.js como base
FROM node:21-alpine3.18

# Habilitar PNPM
RUN corepack enable && corepack prepare pnpm@latest --activate
ENV PNPM_HOME=/usr/local/bin

# Establecer directorio de trabajo
WORKDIR /app

# Copiar archivos de configuración del proyecto
COPY package*.json ./

# Instalar dependencias
RUN apk add --no-cache git
RUN pnpm install