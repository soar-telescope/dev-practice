# Development Practice
Este repositorio es para experimentar con el proceso y flujo de trabajo en equipo para desarrollo de software.

## Fork

En la parte superior de este repositorio, hacer click en fork y ubicar el fork en el espacio personal.

## Clone

Clonar el repositorio personal en el ambiente de desarrollo local, (computador personal o de trabajo)
Excelente, ahora necesitas definir los remotes en tu ambiente de desarrollo. Los remotos son otros lugares donde existe el codigo.

## Definir `remotes`

Primero hay que ver que remotes existen. El simbolo `❯ ` representa el prompt, no hay que escribirlo.
```
❯ git remote -v
origin	git@github.com:simontorres/dev-practice.git (fetch)
origin	git@github.com:simontorres/dev-practice.git (push)
``` 
Aca, `origin` es el nombre del remote y `git@github.com:simontorres/dev-practice.git` es la ubicacion, finalmente `(fetch)` o `(push)` es la operacion o en otras palabras, fetch es descarga y push subida.


Necesitamos agregar otro remote que apunte a la ubicacion donde centralizaremos el codigo. En este caso `git@github.com:soar-telescope/dev-practice.git`. Una de las grandes ventajas que tiene git con respecto a otros sistemas de control de version es que es descentralizado, pero en este caso, la centralizacion no tiene nada que ver con eso.

Para agregar el remote hacemos

```
❯ git remote add upstream git@github.com:soar-telescope/dev-practice.git
```

Aca, `upstream` es solo una convencion, es el nombre que se le da a ese remote en particular y puede ser cualquier cosa.


Repetimos el comando anterior para ver los remotes.

```
❯ git remote -v
origin	git@github.com:simontorres/dev-practice.git (fetch)
origin	git@github.com:simontorres/dev-practice.git (push)
upstream	git@github.com:soar-telescope/dev-practice.git (fetch)
upstream	git@github.com:soar-telescope/dev-practice.git (push)
```

De aqui en adelante, cuando hagamos un push lo haremos a `origin` y cuando hagamos un pull, lo haremos desde `upstream`.

Por ejemplo para hacer un push [Ver Docs](https://docs.github.com/es/get-started/using-git/pushing-commits-to-a-remote-repository)

```
❯ git push origin branch-name
```

Donde `branch-name` es el nombre que le dimos a la branch, como regla general **Nunca** hay que hacer un push a la rama `main`.


Para "bajar" los datos desde un remote hay que hacer un pull [Docs aca](https://docs.github.com/es/get-started/using-git/getting-changes-from-a-remote-repository)

```
❯ git pull upstream branch-name
```

De nuevo, `branch-name` es el nombre de la rama y `upstream` es el nombre del remoto, que puede tomar cualquier valor.
