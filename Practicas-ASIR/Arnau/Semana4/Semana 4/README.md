Usuarios creados: admin // invitado
Grupos creados: alumnos // profesores
Comandos usados: useradd --- // groupadd --- // usermod -aG --- --- // chown // chmod
Permisos: admin -> lectura escritura en profesores / NO en alumnos
invitado -> lectura escritura en alumnos / NO en profesores
Problemas: Usuario admin podia entrar a carpeta alumnos y viceversa
Solución: Reescribir los permisos de las carpetas correctamente
Reflexión: Los permisos es algo fundamental si quieres proteger información sensible de alguna persona.

