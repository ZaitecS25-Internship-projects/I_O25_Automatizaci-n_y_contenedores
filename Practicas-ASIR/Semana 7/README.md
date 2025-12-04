Se instala Docker y Docker Compose y se configura el grupo de usuarios docker para acceso sin sudo. Comprobación: estado activo de Docker (systemctl status docker). 

Se migra la aplicación web de la Semana 6 a un contenedor. Comprobación: acceso al servicio web en el puerto 8080 del host.

Implementamos volúmenes de Docker, los asociamos e inyectamos el contenido HTML. Comprobación: prueba de stop, rm, y run para validar que el contenido web se mantiene. 

Creamos una red privada (red_semana6) y conectamos el contenedor web y un contenedor de prueba. Comprobación: ping exitoso entre contenedores y acceso al servicio web confirmado. 

Creamos el archivo docker-compose.yml para definir y levantar toda la infraestructura con un solo comando. Comprobación: se despliegan todos los servicios (red, volúmenes, contenedores) al usar el comando de Docker Compose.
