# Level 11>12

## Objetivo

Para encontrar la contraseña al siguiente nivel hay que buscar en **data.txt**, teniendo en cuenta que a-z y A-Z han sido rotadas 13 posiciones.

## Herramientas usadas

* `ssh`
* `cat`
* `tr`

## Pasos

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit11@bandit.labs.overthewire.org -p 2220`
2. Usamos \`cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m' para que use ROT13 para desencriptar el mensaje. Nos muestra directamente el mensaje desenctriptado con la contraseña.

## Resources

[ROT13 - Wikipedia](https://en.wikipedia.org/wiki/ROT13).
