
## Ejercicio 1: Despliegue de la aplicación Guestbook


> **Despliegue de Aplicaciones Web** (María Clemente Luengo)

### Paso 1: Clonar el repositorio

Clonamos el repositorio que contiene el archivo `docker-compose.yml`:

```bash
git clone https://josedom24.github.io/curso_docker_2022/sesion3/guestbook.html
```

### Paso 2: Crear y desplegar el escenario

Nos movemos al directorio donde se encuentra el archivo `docker-compose.yml` y ejecutamos el siguiente comando para crear y desplegar el escenario:

```bash
docker-compose up -d
```

### Paso 3: Verificar contenedores en ejecución

Podemos verificar que los contenedores están en ejecución utilizando el comando:

```bash
docker-compose ps
```

### Paso 4: Detener y eliminar el escenario

Para detener y eliminar el escenario, ejecutamos el siguiente comando:

```bash
docker-compose down
```

### Paso 5: Verificar la aplicación

Finalmente, verificamos que la aplicación está funcionando accediendo a ella y dejando una firma.

