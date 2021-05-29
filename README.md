# Ejecutar proyecto, Funcionalidades y Testing

## Como arrancar
Instalar los paquetes de node_modules:
### `npm install`
Crear .env y añadir:
### `PORT = PUERTO EN EL QUE VA A CORRER EL SERVER`
### `DB_CNN = CADENA DE CONEXIÓN A BASE DE DATOS`
### `SECRET_JWT_SEED = PARA LA ENCRIPTACIÓN DE JWT`
Arrancar en localhost:4000 (puerto elegido en la configuración):
Modo Producción:
### `npm start`
Modo Desarrollo:
### `npm run dev`

## Funcionalidades de este proyecto
- Configuración de Express para el entorno del servidor
- Incluimos Nodemon para que el servidor sea "Live Server" y podamos implementar cambios al instante (Modo Desarrollo)
- Configuración de las variables de entorno
- Creación de una carpeta pública donde se expondra el contenido público que ofrezca el servidor
- Creación de Rutas y de Controladores para cada una de nuestras funcionalidades dentro de la aplicación
- Implemtación del parseo JSON
- Estandarizar los códigos de respuestas del Server (Solo puede existir una respuesta por petición)
- Validar con Express Validator y también creación de validaciones personalizadas
- Creación custom middlewares (Los middleares se ejecutan en cascada en la ruta indicada)
- Configuración a MongoDB (Atlas) con Mongoose (modo ORM con Schemas) *Hemos solucionado un problema con las IPs
- Filtrar resultados de los modelos de Mongoose
- Creación de todas las funcionalidades tanto de Auth como de Events
- Encriptación de contraseñas con bcryptjs
- Generar JWT y crear un middleware de validar el JWT
- Configuración CORS (Postman internamente ya tiene mecanismos para saltarse CORS pero nosotros debemos solucionar esto)

## Despliegue Back-End en Heroku recomendaciones:
- Colocar bien el script desde donde va a arrancar la aplicacion -> npm start (Modo Producción)
- Revisar el tema de puertos, Heroku utilizara en el server otros puertos distintos
- Configurar las variables de entorno en el server para mantener la integridad y seguridad de la aplicación
- Con Heroku Logs puedes ver la monitorización del server y depurar errores
