## Configuracion del pipeline para deploy a docker-hub

Se utilizo la herramienta integrada github-actions.

Para implementar este tipo de GitHub Actions en el proyecto, es necesario crear en la raíz del proyecto el directorio .github/workflows. Dentro de este directorio, se definen los workflows que queremos que GitHub reconozca y ejecute.

Pasos para configurar CI/CD en github

- Crear un archivo con extension .yml dentro del directorio .github/workflows (Requisito EXCLUYENTE)
- Escribir dentro del archivo anterior nombrado el evento que va a lanzar el workflows. Por ejemplo un push en una rama, un cambio de un directorio, etc.
- Establecer como variables de entorno el usuario y el token de Docker Hub en settings del repository.
- Recomendacion: utilizar los github-actions oficiales para agilizar la configuracion del pipeline.
- Recomendacion: Ejecutar el workflows como repositorio publico, de lo contrario no funciona.

Para ejecutar el proyecto de cero:

- docker-compose build 
- docker-compose up
- localhost:8800 

Para ejecutar la imagen cargada en docker-hub:

- docker run -p 8800:80 facucc/devops-interview:latest
- localhost:8800

## Links

- [github-Actions](https://docs.github.com/en/actions)
- [docker-actions](https://docs.docker.com/ci-cd/github-actions/)
- [github-marketplace](https://github.com/marketplace)
- [build-push-action](https://github.com/docker/build-push-action)