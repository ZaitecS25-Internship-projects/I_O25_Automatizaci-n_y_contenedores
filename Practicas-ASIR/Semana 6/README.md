# Semana 6 - Proyecto Web

Servidor: Apache2 en Ubuntu 24.04 (robusto y fácil de configurar)
Estructura: /var/www/html con index.html, about.html, contacto.html y css/style.css
Permisos: directorios rwx propietario / r-x grupo; archivos rw propietario / r grupo; propietario www-data

Instalación y configuración:
- Apache actualizado, activo y habilitado
- Firewall UFW abierto para OpenSSH y Apache
- Verificación de acceso

Logs y monitorización:
- Accesos:
  tail -f /var/log/auth.log
  grep sshd /var/log/auth.log
  grep "failed password" /var/log/auth.log
  grep "Accepted password" /var/log/auth.log
  who
  last
- Errores:
  journalctl -p err -b
  journalctl -f
- Códigos HTTP importantes: 200 OK, 404 Not Found, 500 Internal Server Error
- Procesos críticos activos, CPU/RAM bajo uso, sistema estable

Observaciones: intentos de exploits detectados en logs, no afectan la demo

Conclusión:
La web responde correctamente, carga rápido, todas las páginas funcionan y la configuración es segura y lista para la demo.
