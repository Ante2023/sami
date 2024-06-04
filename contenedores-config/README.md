## Para empezar a montar la infraestrutura, primero debemos crear la red bridge a la que se conectarán todos los contenedores

```bash
#1º Creamos la red
docker network create monitoring

#2º creamos y ejecutamos contenedor
 docker-compose -f docker-compose-net.yml up -d 

```

**Sigueiente** -> Leer READEM en "n8n/READEM.md"


