Crear administrador colocando en WSL 2 el comando "sudo adduser admin_1"
Crear cliente con el comando "sudo adduser client_1" 
Confirmar que se crearon bien con los comandos: 
  cat etc/passwd | grep _1: para encontrar los dos usuarios creados
  groups admin_1: si sale "admin_1 sudo users" es que tiene los permisos de administrador bien colocados
  groups client_1: si sale "client_1 users" es que no tiene permisos de usuario, así que está correcto
