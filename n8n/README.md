# Pasos para ejecutar n8n
- 1º Crear volumen **n8n_data**, allí n8n persistirá archivos de Base de Datos SQLite y la clave de cifrado del volumen: 
```bash
sudo docker volume create n8n_data
```
- 2º Crear volumen **traefik_data** para datos de Traefik: 
```bash
sudo docker volume create traefik_data
```
- 3º Crear y ejecutar contenedor
```bash
# sudo docker compose up -d
docker-compose -f docker-compose-n8n.yml up -d
```
- 4º Accediendo al servicio n8n
```bash
http://localhost:5678/setup

# Opcional por si no has creado cuenta aún. Cambiar informacíón  
user: test@test.com
First Name: Test
Last Name: Test
pass: test.test
```
## Observación:
- Se podría ejecutar el contenedor sin sudo. Ya existe 
```bash
 cat /etc/group
 #output
 docker:x:999:dent
```
## Documentacion
[n8n Docs | docker-compose](https://docs.n8n.io/hosting/installation/server-setups/docker-compose/#3-install-docker-compose 'n8n Docs')

**Sigueiente** -> Leer READEM en "metricas/READEM.md"
