## Objetivo

Para encontrar la contraseña al siguiente nivel hay que buscar en _data.txt_ al lado de la palabra **millionth**.

### Herramientas usadas

- `cat`
- `ls`
- `grep`

### Pasos 

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit7@bandit.labs.overthewire.org -p 2220`
2. Usamos `ls` para ver los archivos en el directorio.
3. Usamos `cat data.txt | grep millionth` y nos devuelve directamente la línea donde está la palabra millionth y la clave.
