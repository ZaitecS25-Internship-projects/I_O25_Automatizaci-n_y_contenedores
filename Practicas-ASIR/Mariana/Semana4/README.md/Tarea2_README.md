Crear grupo con el comando "sudo groupadd [nombre_grupo]", en mi caso he puesto sudo groupadd clients
Añadir el usuario creado anteriormente con "sudo usermod -aG clients client_1"
Verificar que se haya añadido correctamente con "cat /etc/group | grep clients"
