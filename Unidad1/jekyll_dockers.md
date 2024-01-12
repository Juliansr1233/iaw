# Sitio Local en Jekyll con Docker

```
Antes de empezar a usar los comandos de este documento deberemos estar con el usuario: root.
```

## Creamos un contenedor Docker con Jekyll:

```
El comando necesario es:
docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll
```

![Img](img/Captura1.png)

## Creamos la estructura de directorios y los archivos necesarios para un proyecto Jekyll nuevo:

Antes de usar este comando debemos estar en la siguiente ruta: /home/usuario

```
El comando necesario es:
docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll new blog
```

![Img](img/Captura2.png)

## Modificamos el archivo gemfile, el la parte de abajo añadimos gem "webrick"

![Img](img/Captura3.png)

## Con este comando nos permite servir de forma local un sitio HTML estatico generado a partir del proyecto:

```
El comando necesario es:
docker run -it --rm -p 4000:4000 -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll serve --force_polling
```
![Img](img/Captura4.png)






