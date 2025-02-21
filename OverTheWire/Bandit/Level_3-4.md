## Objetivo

Para encontrar la contraseña al siguiente nivel hay que encontrar un archivo oculto en el directorio _inhere_.

### Herramientas usadas

- `cat`
- `ls`
- `cd`

### Pasos 

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit3@bandit.labs.overthewire.org -p 2220`
2. Usamos el comando `cd inhere` para ir al directorio.
3. Usamos `ls -a` para ver los archivos. Mediante `-a` vemos los archivos ocultos.
4. Usamos `cat ...Hiding-From-You` para imprimir el contenido.
