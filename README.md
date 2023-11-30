# FCT_3d_server
Proyecto FCT: Servidor de impresión 3D y monitorización
Este repositorio ha sido creado para complementar un proyecto para Proyecto FCT. 


* Instalación y configuración Servidor Impresión 3d con Ubuntu server. 
* Instalación y configuración Servidor de monitorización con Ubuntu server.
-----

## Índice

* [Resumen](#Resumen)
* [Docker-compose octoprint](#Docker-compose_octoprint)
* [Errores conocidos](#errores-conocidos)

-----

## Resumen
La instalación se ha llevado ha llevado a cabo en una raspberry pi que se ocupará de gestionar 2 impresoras 3d mediante la aplicación web octoprint.
A su vez dentro de este equipo se instalarán el software que permita envie la información necesaria para la monitorización del mismo. 
A su vez desde otro equipo se visualizarán los datos recogidos por los diferentes servicios instalados.

### Servicios para la extracción de métricas.
- Node exporter: Se encargará de obtener las métricas de los recursos del servidor.
- cAdvisor: Se encarga de obtener las métricas de los recursos usados por los contenedores.


### Servicios para la centralización de métricas.
- Prometheus: Se encarga de centralizar las información obtenida de las aplicaciones que extraen las métricas
- Promtail: recolecta los registros que será mostrado por Grafana Loki

### Servicio visualizador de métricas
- Grafana: Visualizador de datos.
- Grafana Loki: Herramienta de Grafana para poder mostrar el contenido de los logs indexados.


## Errores conocidos
