# Proyecto INFRAESTRUCTURAS PARALELAS Y DISTRIBUIDAS

Este proyecto es una aplicación de subasta dividida en una API REST para el backend y un frontend construido con React, todo gestionado utilizando Docker y Docker Swarm. A continuación, se describen los pasos para construir y desplegar el sistema utilizando Docker.

## Creadores

- **Miguel Angel Ceballos         - 2259619**
- **Cristian leonardo             - 1968253**
- **Moisés Medina Villa           - 2459709**
- **Nicolas Gutierrez             - 2259515**
- **Karen Jhulieth Grijalba Ortiz - 2259623**



## Comandos para Docker Swarm

A continuación se presentan los comandos necesarios para construir las imágenes Docker, inicializar el Swarm y desplegar la aplicación.

1. **Construir las imágenes Docker para el backend y frontend:**

   ```bash
   docker build -t subasta-back ./SpringSubastAll
   docker build -t subasta-frontend ./fronted_subastall

   docker swarm init
   docker stack deploy --compose-file docker-compose.yml subasta-stack
   
   docker service scale subasta-stack_back=3 #puede fallar pero es cuestion de reintentar
### Notas:
2. **Comandos Docker:** Los comandos proporcionados están listos para ser utilizados. Si tienes algún ajuste en la estructura de tu proyecto, puedes modificar las rutas o los nombres de los servicios.
