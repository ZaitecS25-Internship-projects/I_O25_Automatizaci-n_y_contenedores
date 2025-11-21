Crear estructura de carpetas con: mkdir -p Base_CLientes/Datos_Privados/{01_BD_Usuarios,02_Contratos} Base_Clientes/Comunicacion/{Noticias,Soporte} Base_Clientes/Reportes_Anuales/{Reporte_2024,Reporte_2025}
Para visualizar la estructura, hay que poner: "tree Base_Clientes"
Después asignamos los permisos a cada usuario que hemos creado, conforme a las necesidades de cada sector. Ejemplo de permiso seleccionado: sudo chown admin_1:admin_1 Base_Clientes/Datos_Privados/
Para comprobar que los permisos se haya asignado correctamente se escribe: ls -ld Base_Clientes/Datos_Privados (por ejemplo)
