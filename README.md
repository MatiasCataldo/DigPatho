# Proyecto Frontend - Digpatho

## Mejoras Propuestas y Beneficios

### Mejoras Implementadas
1. **Interfaz de Usuario Mejorada**: Se ha replicado el diseño de la plataforma de referencia, organizando la interfaz con pestañas y un área estructurada para la carga de imágenes.
2. **Selección y Previsualización de Imágenes**: Ahora los usuarios pueden subir imágenes, previsualizarlas y eliminarlas antes de enviarlas.
3. **Manejo de Estado con React**: Se ha optimizado el uso de `useState` para gestionar los datos de imágenes y pestañas de forma eficiente.
4. **Mejor Organización del Código**: Se ha estructurado el código para mejorar su mantenibilidad y escalabilidad.

### Beneficios Esperados
- **Mayor Usabilidad**: La interfaz intuitiva facilita la carga y administración de imágenes.
- **Mejor Experiencia del Usuario**: El sistema de pestañas y botones optimizados mejora la navegación.
- **Escalabilidad**: La estructura modular permite agregar más funcionalidades en el futuro.

---

## Instalación y Ejecución en Local

### Requisitos Previos
- Node.js (versión 18 o superior)
- npm o yarn

### Pasos para Ejecutar el Proyecto
1. Descargar el código fuente y navegar hasta la carpeta del proyecto.
2. Instalar dependencias:
   ```
   npm install

   Dependencias de Producción:
        autoprefixer ^10.4.20
        axios ^1.7.9
        bootstrap ^5.3.3
        next 15.1.6
        react ^19.0.0
        react-dom ^19.0.0
    Dependencias de Desarrollo:
        @eslint/eslintrc ^3
        @types/node ^20
        @types/react ^19
        @types/react-dom ^19
        eslint ^9
        eslint-config-next 15.1.6
        postcss ^8.5.1
        tailwindcss ^3.4.17
        typescript ^5
   ```
3. Iniciar el servidor de desarrollo:
   ```
   npm run dev
   ```
4. Acceder a la aplicación en el navegador en:
   ```
   http://localhost:3000
   ```

---

## Uso de Docker

### Construcción de la Imagen Docker
Para crear la imagen de Docker del frontend, ejecutar:
```
docker build -t digpatho-frontend .
```

### Ejecución del Contenedor
Para ejecutar el contenedor en el puerto 3000:
```
docker run -p 3000:3000 digpatho-frontend
```
Luego acceder a la aplicación en:
```
http://localhost:3000
```

---

## Dockerfile
```dockerfile
# Usar la imagen oficial de Node.js
FROM node:18-alpine

# Establecer el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar los archivos de dependencias y el código fuente
COPY package.json package-lock.json ./

# Instalar dependencias
RUN npm install

# Copiar el resto del código fuente
COPY . .

# Exponer el puerto 3000
EXPOSE 3000

# Comando para iniciar la aplicación
CMD ["npm", "run", "dev"]
```

---

Este archivo README proporciona toda la documentación necesaria para implementar, ejecutar y desplegar la aplicación frontend en un contenedor Docker.

# DigPatho
