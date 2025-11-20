Configurar una IP fija en WSL 2: 
Ejecutar en Ubuntu "hostname -I" para saber la IP actual
Ejecutar "ip route show" para conocer otros datos relevantes
Ejecutar "sudo nano /etc/netplan/89-static.yaml" para configurar la IP en otro pantalla
Confirma los cambios con "sudo netplan apply"
Comprobar que se ha creado correctamente la IP fija con "ip a"
