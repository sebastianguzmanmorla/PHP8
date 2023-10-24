# PHP 8 + Nginx + MySQL

## Instrucciones de uso

1. Clona este repositorio en tu sistema:

   ```bash
   git clone https://github.com/sebastianguzmanmorla/PHP8
   ```

2. Ve al directorio del repositorio:

   ```bash
   cd tu-repositorio
   ```

3. Copia el archivo `.env.example` a `.env` y personaliza las variables de entorno según tus necesidades:

   ```bash
   cp .env.example .env
   ```

   Abre el archivo `.env` en un editor de texto y configura las variables como el nombre de la base de datos, la contraseña, etc.

4. Ejecuta el archivo Docker Compose para crear y ejecutar los contenedores:

   ```bash
   docker-compose --env-file ./.env -f ./.docker/docker-compose.yaml up
   ```

5. Accede a tu aplicación web en tu navegador a través de `http://localhost`. Puedes colocar tus archivos PHP en el directorio `src/`.

6. Para detener los contenedores, ejecuta:

   ```bash
   docker-compose --env-file ./.env -f ./.docker/docker-compose.yaml down
   ```

## Estructura del proyecto

- `.docker/docker-compose.yml`: El archivo de configuración Docker Compose que define los servicios PHP, Nginx y MySQL.

- `src/`: Directorio donde puedes colocar tus archivos PHP.

- `.env.example`: Archivo de ejemplo de variables de entorno. Debes copiarlo y configurarlo como `.env`.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para obtener más detalles.