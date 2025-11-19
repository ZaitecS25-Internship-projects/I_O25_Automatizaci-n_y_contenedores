# Práctica Semana 4 – Usuarios, Grupos y Permisos

## 1️⃣ Objetivos
- Crear usuarios `admin` e `invitado` y grupos.  
- Configurar permisos en `/home/proyecto` y subcarpetas.  
- Probar accesos según permisos.

## 2️⃣ Usuarios y grupos
```bash
cat /etc/passwd | grep -E "admin|invitado"
cat /etc/group | grep -E "grupo_admin|grupo_invitados"


3️⃣ Estructura de carpetas y permisos
sudo mkdir -p /home/proyecto/{docs,config,public}

sudo chown admin:root /home/proyecto/config
sudo chmod 700 /home/proyecto/config

sudo chown root:grupo_admin /home/proyecto/docs
sudo chmod 770 /home/proyecto/docs

sudo chmod 777 /home/proyecto/public
sudo chmod 755 /home/proyecto

4️⃣ Pruebas de acceso
Como admin
sudo -i -u admin
cd /home/proyecto/docs
touch prueba_admin_docs.txt

cd /home/proyecto/config
touch prueba_admin_config.txt

cd /home/proyecto/public
rm -f prueba_admin_public.txt
touch prueba_admin_public.txt
exit
Como invitado
sudo -i -u invitado
cd /home/proyecto/docs      # ❌ Permiso denegado
cd /home/proyecto/config    # ❌ Permiso denegado
cd /home/proyecto/public
touch prueba_invitado_public2.txt
exit
Verificación final
ls -l /home/proyecto/docs
ls -l /home/proyecto/config
ls -l /home/proyecto/public
ls -ld /home/proyecto /home/proyecto/*

5️⃣ Resultados y permisos
Carpeta	Admin	Invitado	Archivos creados
/docs	✔️	❌	prueba_admin_docs.txt
/config	✔️	❌	prueba_admin_config.txt
/public	✔️	✔️	prueba_admin_public.txt, prueba_invitado.txt, prueba_invitado_public2.txt

6️⃣ Problemas y soluciones
su - admin no funcionaba → usar sudo -i -u admin.
touch en /public daba error → eliminar archivo previo con rm -f archivo.
Invitado no podía entrar en /docs ni /config → comportamiento correcto según permisos.
