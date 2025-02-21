## Objetivo

Para encontrar la contraseña al siguiente nivel hay que buscar en _data.txt_ a la única que hay escrita una vez.

### Herramientas usadas

- `ssh`
- `sort`
- `uniq`

### Pasos 

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit8@bandit.labs.overthewire.org -p 2220`
2. Usamos `sort data.txt | uniq -u` y nos imprime la única línea.
