# Utpl.Wso2Docker

Este repositorio está diseñado para facilitar el trabajo con WSO2 en un entorno de Codespace de GitHub en la nube mediante Docker Compose. Sigue los pasos a continuación para arrancar el entorno de desarrollo.

## Requisitos previos
Asegúrate de tener acceso a un entorno de Codespace de GitHub en la nube.

## Pasos para arrancar el entorno desde Codespace

1. **Accede a tu Codespace:**
    Abre este repositorio en un Codespace de GitHub desde tu navegador.

2. **Configura la url del gateway de WSO2:**
    Abre el archivo `deployment.toml` y modifica el valor del enlace: https_endpoint.

    ```bash
    [[apim.gateway.environment.virtual_host]]
    https_endpoint = "https://laughing-spoon-g4q5p747q7w6hw9px-8243.app.github.dev/"
    ```

    Se debe colocar con el nombre del codespace que asigna Github a cada uno.

3. **Inicia el entorno Docker Compose:**
    Ejecuta el siguiente comando para iniciar los servicios definidos en el archivo `docker-compose.yml`:

    ```bash
    docker-compose up -d
    ```

    Este comando descargará las imágenes necesarias, creará y ejecutará los contenedores.

4. **Accede a WSO2 desde tu navegador:**
    Abre tu navegador y visita [https://localhost:9443](https://localhost:9443) para acceder a la consola de administración de WSO2.

5. **Detener el entorno:**
    Cuando hayas terminado de trabajar, puedes detener los contenedores ejecutando:

    ```bash
    docker-compose down
    ```

    Esto detendrá y eliminará los contenedores, pero conservará los datos persistentes.

¡Listo! Ahora puedes trabajar con WSO2 en un entorno de Codespace de GitHub en la nube usando Docker Compose. ¡Disfruta de tu desarrollo!
