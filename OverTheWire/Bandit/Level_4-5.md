## Objetivo

Para encontrar la contraseña al siguiente nivel hay que encontrar un archivo que sea legible para un humano en el directorio _inhere_.

### Herramientas usadas

- `cat`
- `ls`
- `cd`
- `file`

### Pasos 

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit4@bandit.labs.overthewire.org -p 2220`
2. Usamos el comando `cd inhere` para ir al directorio.
3. Usamos `ls` para listar los archivos y ver a qué nos enfrentamos.
4. Vamos probando `file ./-fileXX` para ver qué tipo de archivo es cada uno.
5. El archivo _-file07_ es el único ASCII, por lo que procedemos a hacer `cat ./-file07` para ver el contenido.
