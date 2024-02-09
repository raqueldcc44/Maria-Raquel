# 4 - Redes en Docker

> Raque Cabezas
>
> María Clemente
>
> Despliegue de Aplicaciones

## Ejemplo 1: Despliegue de la aplicación Guestbook

**Crear una red Docker:**

`$ docker network create red_guestbook`

![](../Docker4/ejemplo1-Maria/img/image-20240209092205101.png)

**Ejecutar el contenedor de Redis:**

`$ docker run -d --name redis --network red_guestbook redis`

![](../Docker4/ejemplo1-Maria/img/image-20240209092205101.png)

**Ejecutar el contenedor de GuestBook:**

`$ docker run -d -p 80:5000 --name guestbook --network red_guestbook iesgn/guestbook`

![](../Docker4/ejemplo1-Maria/img/image-20240209092621746.png)

## Ejemplo 2: Despliegue de la aplicación "Temperaturas"

**Red para conectar los dos contenedores:**

`$ docker network create red_temperaturas`

![](../Docker4/ejemplo2-Maria/img/image-20240209095055601.png)

**Ejecutar los contenedores:**
`$ docker run -d --name temperaturas-backend --network red_temperaturas iesgn/temperaturas_backend`

![](../Docker4/ejemplo2-Maria/img/image-20240209101247504.png)



```bash
docker run -d -p 80:3000 --name temperaturas-frontend --network red_temperaturas iesgn/temperaturas_frontend
```

![](../Docker4/ejemplo2-Maria/img/image-20240209101435189.png)
