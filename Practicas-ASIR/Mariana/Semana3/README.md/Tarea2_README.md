Abrir PowerShell como administrador
Abrir la distribución de Ubuntu instalada y ejecutar el comando "ifconfig" para descubrir la dirección IP utilizada
Intalar los net tools para poder configurar la NAT de Ubuntu con "sudo apt install net-tools"
En PowerShell ejecutar "netsh interface portproxy add v4tov4 listenport=3000 listenaddress=0.0.0.0 connectport=3000 connectaddress=$WSL_IP"
Ir a Firewall de Windows Defender -> Activar o desactivar el Firewall de Windows Defender -> Reglas de Entrada -> Nueva regla 
En Nueva regla, crear regla para el puerto seleccionado, en este caso 3000
