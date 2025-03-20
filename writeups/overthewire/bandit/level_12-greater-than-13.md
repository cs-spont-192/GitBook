## Objetivo

Para encontrar la contraseña al siguiente nivel hay que buscar en **data.txt**, el cual es un hex dump (volcado hexadecimal) que ha sido comprimido repetidas veces. 

### Herramientas usadas

- `ssh`
- `mktemp`
- `cp`
- `mv`
- `xxd`
- `file`
- `gunzip`
- `bzip2`
- `tar`



### Pasos 

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit12@bandit.labs.overthewire.org -p 2220`
2. Usamos `mktemp -d` para crear una carpeta temporal.
3. Usamos `cp data.txt /tmp/tmp.XXXXX` para hacer una copia del archivo en la nueva carpeta.
4. Usamos `mv data.txt data_copy.txt` para cambiar el nombre al archivo.
5. Usamos `xxd -r data_copy.txt > new_data` para convertir de hexadecimal a binario.
6. Usamos `file new_data` para ver qué tipo de archivo es (comprimido de gzip) y los detalles.
7. Usamos `mv new_data new_data.gz` para convertirlo.
8. Usamos `gunzip new_data.gz` para descomprimirlo.
9. Usamos `file new_data` para ver el formato (bzip2) y los detalles.
10. Usamos `mv new_data.bz2` para crear el .bz2.
11. Usamos `bzip2 -d new_data.bz2` para extraerlo.
12. Usamos `file new_data` para ver el formato (gzip) y los detalles.
12. Usamos `mv new_data new_data.gz` para convertirlo.
13. Usamos `gunzip new_data.gz` para extraerlo.
14. Usamos `file new_data` para ver el formato (POSIX tar archive GNU).
15. Usamos `mv new_data new_data.tar` para convertirlo.
16. Usamos `tar -xf new_data.tar` para descomprimirlo.
17. Usamos `ls` para comprobar los resultados; un archivo nuevo .bin.
18. Usamos `file data5.bin` y comprobamos que es otro archivo tar.
19. Usamos `tar -xf data5.bin` y nos extrae un data6.bin.
20. Usamos `file data6.bin` y vemos que es un bzip2.
21. Usamos `bzip2 -d data6.bin`.
22. Usamos `file data6.bin.out` y comprobamos que es un tar.
23. Usamos `mv data6.bin-out data_6.tar` para convertirlo.
24. Usamos `tar -xf data_6.tar` y nos da un data8.bin.
25. Usamos `file data8.bin` y nos comprobamos que es un gzip.
26. Usamos `mv data8.bin data8.gz` para convertirlo.
27. Usamos `gunzip data8.gz` para extrarelo.
28. Vemos que el archivo final es un ASCII que contiene la contraseña al siguiente nivel.



### Resources

[ROT13 - Wikipedia](https://en.wikipedia.org/wiki/Hex_dump).
