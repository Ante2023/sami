## Para empezar a montar la infraestrutura, primero debemos crear la red bridge a la que se conectarán todos los contenedores
```bash
docker network create monitoringç
```

RESUMEN:
1º levantar contenedores-config/docker-compose-net.yml
 docker-compose -f docker-compose-net.yml up -d

2º crear volumenes y levantar  n8n/docker-compose-n8n.yml
    crear volumenes
   docker-compose -f docker-compose-n8n.yml up -d

3º levantar /metricas/docker-compose-metricas.yml
   docker-compose -f docker-compose-prometheus.yml up -d
