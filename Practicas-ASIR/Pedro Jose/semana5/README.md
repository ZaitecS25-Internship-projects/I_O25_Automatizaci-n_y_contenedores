
Resumen de la práctica – Semana 5 (SSH) 
En esta práctica se configura el acceso remoto seguro mediante SSH en Ubuntu.
Se realiza la instalación del servicio, la obtención de la IP, la conexión inicial con contraseña y la configuración de autenticación por clave pública para permitir acceso sin contraseña.
Pasos realizados:
Instalación y activación de SSH
sudo apt install openssh-server
sudo systemctl enable --now ssh
Se verifica el servicio con systemctl status ssh.
Obtención de la dirección IP
ip a
IP principal usada: 192.168.1.210
Conexión al servidor con contraseña
ssh pedrocozar@192.168.1.210
Acceso exitoso solicitando password.
Generación de par de claves SSH
ssh-keygen -t rsa -b 4096 -f ~/.ssh/id_rsa_semana5
Clave creada correctamente.
Copia de la clave pública al servidor
ssh-copy-id -i ~/.ssh/id_rsa_semana5.pub pedrocozar@192.168.1.210
Instalación de la clave exitosa.
Conexión sin contraseña
ssh -i ~/.ssh/id_rsa_semana5 pedrocozar@192.168.1.210
Acceso automático sin pedir password.
(Opcional) Mejora de seguridad
Desactivar autenticación por contraseña en sshd_config.
