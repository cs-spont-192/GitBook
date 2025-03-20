# Level 5>6

## Objetivo

Para encontrar la contraseña al siguiente nivel hay que encontrar un archivo que sea tenga las siguientes características en el directorio _inhere_:

human-readable, 1033 bytes, no ejecutable

## Herramientas usadas

* `ssh`
* `cat`
* `ls`
* `cd`
* `find`
* `du`

## Pasos

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit5@bandit.labs.overthewire.org -p 2220`
2. Usamos el comando `cd inhere` para ir al directorio.
3. Usamos `ls` para listar los archivos y ver a qué nos enfrentamos.
4. Usamos `find -size 1033c` y nos arroja el único archivo que cumple esa característica con la contraseña.
5. Alternativamente, se puede usar `du -b -a | grep 1033` de modo que busque con `du -b -a` en bytes y por los escondidos.
