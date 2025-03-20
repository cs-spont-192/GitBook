# Level 1>2

## Objetivo

Para encontrar la contraseña al siguiente nivel hay que encontrar un archivo llamado **-** en el directorio _home_.

## Herramientas usadas

* `ssh`
* `cat`

## Pasos

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit1@bandit.labs.overthewire.org -p 2220`
2. Usamos el comando `cat ./-` para ver el contenido. `./` viene a ser el actual directorio.
