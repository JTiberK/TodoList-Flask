## Aplicación de gestión de listas de tareas con Flask en Docker

_JTiberK_
_10-07-2025_


Esta sencilla aplicación de **Flask** permite gestionar listas de tareas. Permite a los usuarios registrarse, iniciar sesión y gestionar sus notas o tareas. Está desarrollada con **Flask**, **Flask-SQLAlchemy**, **Flask-Login** y **Python-dotenv** para gestionar la configuración del entorno.

### Características

- Autenticación (Registrarse, Iniciar sesión, Cerrar sesión)
- Añadir, completar y eliminar notas
- Almacenamiento permanente de datos con SQLite y SQLAlchemy
- Notificaciones Flash para mostrar comentarios a los usuarios
- Seguimiento del estado de finalización de las notas


### Tecnología utilizada

- flask
- Flask-SQLAlchemy
- flask-login
- python-dotenv


### Puesta en marcha

**Requisitos**

- Python 3.8 original, actualizado a Python 3.13.3
- pip

**Repositorio Original**
```bash
git clone https://github.com/knguyen-1411/todolist-flask.git
cd todolist-flask
```

**Creación de entorno virtual**
```bash
python -m venv venv

.\venv\Scripts\activate
```
El módulo venv admite la creación de «entornos virtuales» ligeros, cada uno con su propio conjunto independiente de paquetes de Python instalados en sus directorios site. Se crea un entorno virtual sobre una instalación existente de Python, conocida como la «base» del entorno virtual de Python y, opcionalmente, se puede aislar de los paquetes en la base del entorno, así que solo están disponibles los instalados explícitamente en el entorno virtual.

```bash
pip install -r requirements.txt
```
Los archivos de requisitos se utilizan para almacenar el resultado de la congelación de pip con el fin de lograr instalaciones repetibles . En este caso, el archivo de requisitos contiene una versión fija de todo lo instalado durante la ejecución.pip freeze

**Set .env**

- KEY=your-secret-key
- DB_NAME=todolist.db

¿Qué significa "Set .env"?
La instrucción "Set .env" indica que debes crear un archivo llamado .env en la raíz del proyecto. Este archivo almacenará variables de entorno que la aplicación necesita para funcionar correctamente.

```bash
# Run app
python app.py
```
Lanzar la aplicación de Python-Flask

### Dockerización

Este proyecto tiene `Dockerfile` y un `compose.yml` (o docker-compose.yml), entonces está listo para ejecutarse en Docker.
Sin embargo, no aparecerá en Docker Desktop hasta que lo levantes por primera vez.

Aquí tienes los pasos para que tu proyecto aparezca en Docker Desktop y puedas gestionarlo desde la interfaz:

1. Abre una terminal en la carpeta de tu proyecto
Asegúrate de estar en la misma carpeta donde están Dockerfile y compose.yml.

2. Inicia los servicios con Docker Compose
Ejecuta el siguiente comando:

```powershell
docker compose up -d
```

### Verifica en Docker Desktop

Abre Docker Desktop.

Ve a la sección Containers (Contenedores).

Ahora deberías ver tu proyecto y los servicios definidos en el archivo compose.yml.

3. (Opcional) Verifica desde la terminal

Puedes ver los contenedores en ejecución con:

```powershell
docker ps
```

Y las imágenes con:

```powershell
docker images
```

4. Detén los servicios cuando quieras
Desde la terminal, puedes detenerlos con:

```powershell
docker compose down
```

**Links** <br>
https://pip.pypa.io/en/stable/ <br>
https://www.docker.com/ <br>
https://hub.docker.com/ <br>
https://tutorialshub.org/docker-commands/


#### Para completar
```text
docker ps -a -q
```

_Completado 19/10/2024_

