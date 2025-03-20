# Level 6>7

## Objetivo

Para encontrar la contraseña al siguiente nivel hay que encontrar un archivo que sea tenga las siguientes características en el servidor:

el user owner es bandit7, el user group es bandit6, 33 bytes

## Herramientas usadas

* `ssh`
* `cat`
* `file`

## Pasos

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit6@bandit.labs.overthewire.org -p 2220`
2. Usamos `find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null` para que nos muestre directamente el archivo que buscamos.
