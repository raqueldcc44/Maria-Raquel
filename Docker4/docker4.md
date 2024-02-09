# 4 - Redes en Docker

> Raque Cabezas
>
> María Clemente
>
> Despliegue de Aplicaciones

## Ejemplo 1: Despliegue de la aplicación Guestbook

**Crear una red Docker:**

`$ docker network create red_guestbook`

![](/home/linux/Escritorio/Maria-Raquel/Docker4/ejemplo1-Maria/img/image-20240209092205101.png)

**Ejecutar el contenedor de Redis:**

`$ docker run -d --name redis --network red_guestbook redis`

![](/home/linux/Escritorio/Maria-Raquel/Docker4/ejemplo1-Maria/img/image-20240209092205101.png)

**Ejecutar el contenedor de GuestBook:**

`$ docker run -d -p 80:5000 --name guestbook --network red_guestbook iesgn/guestbook`

![](/home/linux/Escritorio/Maria-Raquel/Docker4/ejemplo1-Maria/img/image-20240209092621746.png)
