# Level 9>10

## Objetivo

Para encontrar la contraseña al siguiente nivel hay que buscar en **data.txt** una string legible para un humano y precedida de varios **=**.

## Herramientas usadas

* `ssh`
* `strings`
* `grep`

## Pasos

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit9@bandit.labs.overthewire.org -p 2220`
2. Usamos `strings data.txt | grep "="` para que nos muestre por líneas todas las líneas que llevan incluido al menos un =. En este caso vemos en una de ellas la contraseña para el siguiente nivel.
