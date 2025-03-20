## Objetivo

Para encontrar la contraseña al siguiente nivel hay que buscar en **data.txt** que tiene datos codificados con _base64_.

### Herramientas usadas

- `ssh`
- `base64`

### Pasos 

1. Nos conectamos a la máquina usando el siguiente comando: `ssh bandit10@bandit.labs.overthewire.org -p 2220`
2. Usamos `base64 -d data.txt` y nos devuelve el contenido descifrado el cual es la contraseña para el siguiente nivel.
