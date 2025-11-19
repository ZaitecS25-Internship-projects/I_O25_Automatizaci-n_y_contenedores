# Semana 3 – Pedro Jose

## 1. Descripción
En esta práctica se configuraron dos máquinas virtuales (VM1 y VM2) y se realizaron pruebas de conectividad entre ellas y con el router. Se incluyen configuraciones de red y resultados de ping.

---

## 2. Archivos incluidos
- `ip-a-vm1.txt` – Dirección IP asignada a VM1.  
- `ip-a-vm2.txt` – Dirección IP asignada a VM2.  
- `netplan-vm1.txt` – Configuración de red de VM1.  
- `netplan-vm2.txt` – Configuración de red de VM2.  
- `ping-router-vm1.txt` – Resultado del ping de VM1 al router.  
- `ping-router-vm2.txt` – Resultado del ping de VM2 al router.  
- `ping-vm1-desde-vm2.txt` – Resultado del ping de VM1 desde VM2.  
- `ping-vm2-desde-vm1.txt` – Resultado del ping de VM2 desde VM1.  
- `README.md` – Documento explicativo.

---

## 3. Problemas encontrados y soluciones

1. **Conectividad entre VM1 y VM2**
   - Inicialmente los pings entre VM1 y VM2 fallaban.  
   - Se detectó que la configuración de red no estaba aplicada correctamente.  
   - **Solución:** ejecutar `sudo netplan apply` en ambas máquinas y verificar las IPs.

2. **Subida de archivos a GitHub**
   - Intentos de subir vía terminal fallaron por problemas de autenticación (HTTPS y Zsh con espacios).  
   - **Solución:** se subieron los archivos usando la opción **Upload files** en la web de GitHub.

---

## 4. Comandos principales ejecutados en la práctica

```bash
# Verificar IP de VM1 y VM2
ip a

# Configurar red con netplan
sudo nano /etc/netplan/01-netcfg.yaml
sudo netplan apply

# Comprobar conectividad con el router
ping <IP-router>

# Comprobar conectividad entre VMs
ping <IP-VM2>  # desde VM1
ping <IP-VM1>  # desde VM2
