# Monitorizando métricas de rendimiento de contendor
## Docker como objetivo de monitoreo por Prometehus

Las **métricas de rendimento** de un contenedor Docker pueden ser monitoreadas si configuramos el daemon docker en ```/etc/docker/daemon.json``` para que las exponga como servicio por **"127.0.0.1:9323"** . Además este contenedor deberá ser registrado como objetivos para **prometheus** desde **prometheus.yml** .
```json
# Contenido de archivo "/etc/docker/daemon.json"
{
  "metrics-addr": "127.0.0.1:9323"
}
```
Docker tomará esta configuración y expondrá métrias en **formato compatible con Prometheus** en el puerto 9323 e interface del host-anfitrión del host-anfitrión.  

**Prometheus**: Software con un set de herramientas de alertas y monitero de objetivos.    

## Creando el contenedor de prometheus
```bash
# docker compose pu -s
  docker-compose -f docker-compose-prometheus.yml up -d

```
## Accediendo al servicio web de prometheus
```bash
http://localhost:9090/
```
## Accediendo las metricas de app.py
```bash
http://localhost:5000/metrics
```

## Accediendo las metricas de docker
```bash
http://localhost:9323/metrics
```